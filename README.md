# Joggy

## Enhancing Safety Through Secure Outdoor Activity Solutions

---

### Phase 0 - System Overview

The proposed mobile app is designed to enhance personal safety for individuals engaged in outdoor activities such as jogging or working out in public spaces. Joggy aims to improve personal and community safety by allowing users to share location data in emergencies, report problems, and receive real-time assistance. 

**Key Features:**
1. **User Registration Module**: Collects user details and emergency contact information.
2. **Location Tracking System**: Displays running paths, outdoor gyms, and shares real-time location data with custom emergency contacts.
3. **Payment System**: Enables users to access payment services securely.
4. **Personal Verification for Login**: Ensures user legitimacy through verification processes.
5. **Emergency Notification System**: Sends alerts, including real-time navigation and user details, to emergency contacts and/or administrators.
6. **Secure Cloud Database Integration**: Provides secure storage for user and administrative data.

---

### Phase 1 - Business Value of the System

To visualize the app's use cases, assets, and business goals, draw.io was utilized, and potential loss events from breaches or vulnerabilities were evaluated using the **Yacraf methodology**. This ensures alignment with organizational objectives while proactively addressing risks.

#### **Business Goals:**
- Ensure reliable notifications by sending accurate alerts to emergency contacts.
- Maintain secure data management by protecting users' information in secure cloud services.
- Create community awareness of danger zones by allowing users to report and share information.
- Implement a secure payment system.

#### **Use Cases:**
- Sending emergency alerts to notify contacts during critical situations.
- Sharing real-time locations for safety purposes.
- Community reporting of danger areas for user awareness.

#### **Assets:**
- **Mobile App**: User-facing interface.
- **App Server**: Processes data, notifications, and real-time updates.
- **Cloud Database**: Stores sensitive information and hazard reports.
- **Location Tracking System**: Enables real-time mapping and navigation.

#### **Actors:**
- **Users**: Individuals ensuring their personal safety.
- **Admins**: Manage notifications, hazard reports, and data security.

---

### Phase 2 - System Definition and Decomposition

**Key Components:**

1. **Jogging App**: User-facing interface for location sharing, notifications, and problem reporting.
   - Secure communication via HTTPS.

2. **Authentication Server**: Authorizes users using OAuth 2.0 and multi-factor authentication.

3. **App Server Backend**: Coordinates data flow securely with APIs.

4. **Cloud Service**: Stores sensitive data with AES-256 encryption and TLS 1.3 connections.

5. **Emergency Notification System**: Sends alerts via SMS and in-app notifications using reliable messaging protocols.

#### **System Assets Table:**


### Phase 3 - Threat Analysis

Using the **Yacraf methodology**, the following threats were identified:

#### **Threat Profiles:**
- **APT29**: State-sponsored, targets critical infrastructure.
- **FIN7**: Financially motivated, targets payment systems.
- **Lazarus Group**: Advanced state-sponsored actors targeting user data.

#### **Key Abuse Cases:**
1. Exploiting real-time location data to stalk users.
2. Triggering false alerts or overloading the notification system.
3. Stealing user profiles, emergency contacts, and financial data.


---

### Phase 4 - Attack and Resilience Analysis

#### 1. **Exploiting Location Data:**
- **Vulnerabilities**: Weak API authentication, misconfigured endpoints, and outdated encryption.
- **Mitigation**: Implement rate limiting, API monitoring, and upgrade to TLS 1.3.

#### 2. **Triggering False Alerts:**
- **Vulnerabilities**: Lack of anomaly detection and rate limiting.
- **Mitigation**: Introduce rate limits, diversify notification channels, and add anomaly detection systems.

#### 3. **Data Breaches:**
- **Vulnerabilities**: Weak authentication, misconfigured cloud services.
- **Mitigation**: Use robust authentication (MFA), SQL injection protection, and encrypted storage.

---

### Phase 5 - Risk Assessment and Recommendations

1. **Upgrade Encryption**:
   - Use AES-256 for data at rest and TLS 1.3 for data in transit.
2. **Strengthen Authentication**:
   - Multi-factor authentication (MFA) for all users.
3. **Secure APIs**:
   - Implement rate limiting, anomaly detection, and input validation.
4. **Cloud Service Hardening**:
   - Automate patch management and enforce secure configurations.
5. **Regular Security Audits**:
   - Conduct penetration tests and vulnerability scans.

By implementing these recommendations, the Joggy app can maintain a strong security posture and deliver a safe, reliable experience.

---

### References:
1. [Draw.io - Online Diagram Software](https://app.diagrams.net)
2. [Yacraf Framework](https://yacraf.org)
3. [OWASP API Security Top 10](https://owasp.org/API-Security/)
4. [MITRE ATT&CK Groups](https://attack.mitre.org/groups/)
