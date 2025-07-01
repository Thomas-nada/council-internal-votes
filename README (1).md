# **Intersect Constitutional Council Voting Tool**

A simple, secure, and serverless web application for managing governance votes for a small council or committee. This tool is built with vanilla HTML, JavaScript, and Tailwind CSS, and it uses Google Firebase's Firestore as its backend for data storage and authentication.

**Live Demo:** [https://thomas-nada.github.io/council-internal-votes/](https://thomas-nada.github.io/council-internal-votes/)

## **Features**

* **Secure, Role-Based Access:** Members log in with a unique, admin-set code. A dedicated Admin role has exclusive privileges.  
* **Dynamic Governance Actions:** The Admin can create, edit, archive, and delete voting proposals directly from the UI.  
* **Real-Time Voting & Summaries:** Members can cast and change their votes until the deadline. All users see a live summary of the vote counts and quorum status for each proposal.  
* **Deadline Management:** Actions have optional deadlines with a color-coded visual indicator (Green/Yellow/Red) to show urgency.  
* **Member Self-Service:** Logged-in members can change their own login codes.  
* **Comprehensive Audit Log:** A detailed, de-anonymized audit log is available to the Admin, tracking all major events (action creation, edits, votes cast, etc.).  
* **Data Export:** The full audit log can be downloaded as a CSV file for record-keeping.  
* **Global Admin Controls:** The Admin can reset all votes or the entire audit log with a single click (protected by confirmation).

## **Setup**

This application is serverless but requires a Google Firebase project for the backend. To set up your own instance, follow these steps:

#### **1\. Create a Firebase Project**

* Go to the [Firebase Console](https://console.firebase.google.com/) and create a new project.

#### **2\. Enable Firebase Services**

* **Authentication:** In your project, go to **Build \> Authentication \> Sign-in method** and enable the **Anonymous** provider.  
* **Firestore Database:** Go to **Build \> Firestore Database** and create a new database. Start in **production mode**.

#### **3\. Set Up Security Rules**

* In the Firestore Database section, go to the **Rules** tab and paste the contents of the firestore.rules file from this repository. Publish the changes.

#### **4\. Connect the App**

* In your Firebase project's **Project settings**, create a new **Web App**.  
* Firebase will give you a firebaseConfig object. Copy this object.  
* In the index.html file, find the existing firebaseConfig variable and replace it with the one you just copied.

#### **5\. Create Initial Admin User**

* In the Firestore **Data** tab, manually create a collection named login\_codes.  
* Inside login\_codes, create a document with the ID Admin.  
* Add a field to this document named code and set its value to your desired secure admin password.

You can now open the index.html file, log in as Admin with the code you just set, and begin managing the application.

## **License**

This project is licensed under the Apache License 2.0. See the LICENSE file for details.

