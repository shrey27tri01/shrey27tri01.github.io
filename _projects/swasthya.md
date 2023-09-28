---
layout: project
title: Swasthya Suraksha, a streamlined ABDM framework
subtitle: Seamless exchange of medical records across establishments
---

The Swasthya Suraksha framework aims to provide a trusted channel to connect patients, doctors, hospitals, and the consent manager. It connects the establishments to share the health data, given the patient’s consent. Each entity is assigned a unique ID called the Swasthya Suraksha ID(SSID). The Swasthya Suraksha framework is primarily composed of the gateway, the database, the Patient App, the Hospital App and Consent Manager. The gateway is the sole communication medium for all the patient and hospital applications.

The database maintains the user and authentication details. A patient/establishment registers in our app and gets a Swasthya Suraksha ID(SSID) and gets connected to our central gateway. In Patient App, patients can see the list of consents and then have a choice to approve/reject/revoke the consent initiated by doctor/establishment. In Hospital App, doctors can request a health record, fetch all consents, and create an EHR (Electronic Health Record).

#### The Gateway

The gateway is a complete backend service that all parties are required to communicate with. The gateway can register and authenticate patients, accept new consent request from HIU (Health Information User), accept data request with prior consent from HIU, place  data request to HIP (Health Information Provider), handle accept, revoke, or reject consent request from patient, fetch consents given the SSID.

#### Registration and Authentication

The patients can register via the patient application. They are required to fill necessary demographic data along with their password and authentication pin. The user will receive an OTP on the registered mobile number. On entering the OTP, the gateway verifies the OTP and generates a unique 12-digit SSID.

The patients can login via the patient application. The patient enters the SSID and password for authentication. JWT (JSON Web Token) is used to maintain a user session.

#### Consent Request from HIU

The doctor can place a new consent request for patient data. The hospital application is required to provide the doctor SSID, HIU SSID, patient SSID, and HIP SSID. The gateway validates the existence of all SSIDs. On validation, the gateway creates a new consent object with the shared fields and places a request to the consent manager to add a new pending consent.

#### Data Request with Prior Consent
If the hospital is already in possession of a consent object for the required data and the doctor wishes to fetch new data, they can place a request to the gateway to directly fetch data from the HIP without involving the patient.

The HIU provides the consent ID of the consent object associated with the data required. The gateway fetches the consent object from the CM (Consent Manager) and verifies it with the CM. On verification, the gateway places a request to the HIP to send the data.

#### Send Data Request

The gateway places the send data request to the HIP by sharing the consent object and the URL at which they can post the data to HIU.

#### Fetch Consents

The patient dashboard calls the gateway to fetch consents. The gateway requests the CM to share the consent objects given the patient SSID. This fetches all pending, approved and revoked consents.

#### Approve, Reject and Revoke Consent

If a consent object is pending, i.e., the object is yet to be approved, the patient can approve it by filling the necessary fields and providing the authentication pin. The gateway shares this pending consent object with the filled fields and the authentication pin to the consent manager. The CM verifies the pin and saves the consent object, and is said to be approved. The gateway also shares this new consent object with the HIU and HIP.

If a consent object is approved, the patient can revoke the consent. The CM changes the status of the consent object to pending (sets approved to false). The gateway also updates the status of consent in HIU and HIP.
The patient can also reject the consent, which deletes the consent object.


#### Implementation

Check out the project report and other links [here](https://iiitborg-my.sharepoint.com/personal/shrey_tripathi_iiitb_org/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fshrey%5Ftripathi%5Fiiitb%5Forg%2FDocuments%2FHAD%20Final%20Report%2Epdf&parent=%2Fpersonal%2Fshrey%5Ftripathi%5Fiiitb%5Forg%2FDocuments&ga=1).