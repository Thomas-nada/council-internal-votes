# Intersect Constitutional Council Voting Tool - README

## 1. Introduction

Welcome to the Intersect Constitutional Council Voting Tool. This application provides a secure and real-time platform for council members to vote on governance actions. It features distinct roles for regular members and an administrator, each with specific capabilities to ensure a smooth and transparent voting process.

This guide will walk you through the functionalities available to both Members and the Admin.

---

## 2. Getting Started: Logging In

The tool can be accessed at the following URL:
[**https://thomas-nada.github.io/council-internal-votes/**](https://thomas-nada.github.io/council-internal-votes/)

All users, regardless of their role, begin at the same login screen.

1. **Open the Tool:** Navigate to the URL above. You will be presented with a login modal.
2. **Select Your Name:** Click the dropdown menu and select your name from the list (e.g., "Hosky", "Ian", "Admin").
3. **Enter Your Code:** In the password field below, enter the unique, secure code assigned to you.
4. **Click Login:** If the name and code are correct, you will be logged into the main application.

If you enter an incorrect code, an error message will appear.

---

## 3. Member Guide

As a council member, your primary role is to review and vote on active governance proposals.

### 3.1. The Main Dashboard

Upon logging in, you'll see your dashboard, which includes:

* **Your Voting Summary:** A quick overview at the top showing your pending votes, total votes cast, and a breakdown of your "Yes," "No," and "Abstain" votes.
* **Active Actions:** The main section lists all governance actions currently open for voting.
* **View Toggle:** Buttons to switch between "Active" and "Archived" proposals.

### 3.2. How to Vote

For each action card in the "Active" view, you will find:

* **Title and Links:** The proposal title, its unique ID, and direct links to the Proposal, Working Document, and the GovTool entry.
* **Voting Buttons:** A set of "Yes," "No," and "Abstain" buttons. To cast your vote, simply click the desired option. Your selection will be highlighted with a "selected" style, and your vote is saved instantly. You can change your vote at any time before the deadline.
* **Deadline Timer:** A timer indicates how long is left until voting closes. Once the deadline passes, the voting buttons will be disabled.
* **Live Results Summary:** Below the voting buttons, you can see a live summary of the council's votes, including the total "Yes," "No," and "Abstain" counts, whether the quorum has been met, and the current projected outcome.

### 3.3. Pre-Vote Checklist

Some proposals may include a "Pre-Vote Checklist" to ensure all aspects have been reviewed.

* Click the **"Pre-Vote Checklist"** header on an action card to expand it.
* Check the boxes for each item (e.g., "Wallet Address," "IPFS") as you verify them.
* Your checklist progress is saved automatically and is unique to you.

### 3.4. Viewing Archived Actions

To see past proposals:

1. Click the **"Archive"** button in the view toggle at the top of the page.
2. The list will now show all closed and archived actions.
3. On each card, you will see your final vote for that proposal and the final results summary.

### 3.5. Changing Your Login Code

For security, you can change your personal login code at any time.

1. Click the **Key Icon** in the header.
2. A modal will appear. Enter your desired new code in both fields.
3. Click "Save Changes." Your login code is now updated.

---

## 4. Admin Guide

As the Administrator, you have full control over managing governance actions and users.

### 4.1. The Admin Panel

The collapsible "Admin Tools" panel is visible only to you. Click the header to expand or collapse it. It is divided into two main sections: **Manage Actions** and **User Access & Global Controls**.

### 4.2. Managing Actions

#### Adding a Single Action

1. Fill in the fields: `Gov Action ID`, `Title`, and any relevant links.
2. Select a `Voting Deadline` from the dropdown of epoch end times.
3. Check `Include Pre-Vote Checklist` if required.
4. Check `Save as Draft` if you want to prepare the action without making it visible to members yet. If unchecked, it will go live immediately.
5. Click **"Add New Action"**.

#### Bulk Importing Actions via CSV

1. Create a CSV file with the following headers: `id`, `title`.
2. Optional headers include: `govToolLink`, `proposalLink`, `workingDocLink`, `deadline` (in `YYYY-MM-DD HH:mm` format), and `includeChecklist` (`TRUE` or `FALSE`).
3. Click **"Choose File"** and select your CSV.
4. Click **"Import from CSV"**. All actions in the file will be imported as **drafts**.

#### Editing and Publishing Actions

* **Edit:** Click the **Pencil Icon** on any action card (draft, active, or archived) to open a modal where you can edit its details.
* **Publish a Draft:** In the "Drafts" view, click the **"Publish"** button on a draft card to make it active and visible to all members for voting.

#### Archiving and Deleting Actions

1. In the "Manage Action(s)" section of the admin panel, use the multi-select box to choose one or more actions.
2. **Archive:** Click **"Archive Selected"** to move active proposals to the archive, effectively closing the vote. This is the standard way to end a voting period.
3. **Delete:** Click **"Delete Selected"** to **permanently remove** an action and all of its associated votes. This action is destructive and should be used with extreme caution.

### 4.3. Viewing Detailed Results

While members see a summary, you can see detailed results for any non-draft proposal.

* Simply click anywhere on an "Active" or "Archived" action card.
* A modal will appear showing:
  * The final council outcome.
  * A breakdown of "Yes," "No," and "Abstain" votes.
  * Quorum status.
  * A list of every member and their specific vote.
  * The relevant links for the proposal for quick access.

### 4.4. User and Global Management

#### User Access

1. Select a member from the "Select Member to Manage" dropdown.
2. You can see if their code is set.
3. To set or reset a member's code, type a new code in the input field and click **"Set/Reset"**.

#### Audit Log and Activity

* **Recent Activity:** The feed shows the latest actions taken in the tool, such as votes cast and actions created.
* **Download Audit Log:** Click the **"Download CSV"** button to get a complete, timestamped log of every action ever taken in the tool for record-keeping.

#### Global Controls (Use with Caution)

* **Reset All Votes:** This button will **permanently delete every vote** from every member for every proposal.
* **Reset Audit Log:** This button will **permanently delete the entire activity log**.

Both actions require confirmation and are irreversible.
