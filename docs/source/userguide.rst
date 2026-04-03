Table of Contents
=================

1.  `Introduction & Overview <#introduction-overview>`__

2.  `Getting Started <#getting-started>`__

3.  `Dashboard <#dashboard>`__

4.  `Biospecimen Management <#biospecimen-management>`__

5.  `Storage Hierarchy <#storage-hierarchy>`__

6.  `User Management <#user-management>`__

7.  `Access Control <#access-control>`__

8.  `Reporting & Analytics <#reporting-analytics>`__

9.  `Activity Log & Audit Trail <#activity-log-audit-trail>`__

10. `Notifications <#notifications>`__

11. `Profile & Settings <#profile-settings>`__

12. `Data Export <#data-export-1>`__

13. `Keyboard Shortcuts & Tips <#keyboard-shortcuts-tips>`__

Introduction & Overview
=======================

What is iCCaRE Biobank?
-----------------------

   iCCaRE (Integrated Clinical Care and Research Environment) Biobank is
   a comprehensive web-based system designed to manage biological
   specimens and associated data for research purposes. The system
   provides:

- **Specimen Management** — Register, track, and manage biosamples
  throughout their lifecycle

- **Storage Organization** — Hierarchical storage structure from regions
  to individual freezer positions

- **Access Control** — Role-based permissions with global, regional, or
  site-level access

- **Workflow Automation** — Approval workflows for specimen movements,
  transfers, and disposals

- **Audit Trail** — Complete chain of custody and activity logging for
  regulatory compliance

- **Reporting & Analytics** — Dashboard metrics, utilization reports,
  and data export capabilities

Key Capabilities
----------------

- Register specimens with a guided 4-step wizard and comprehensive
  metadata

- Track specimen movements between storage locations with approval
  workflows

- Manage storage infrastructure (regions, sites, freezers, racks, boxes)

- Control user access at global, regional, or site levels with
  fine-grained permission flags

- Monitor inventory with real-time dashboard and utilization metrics

- Generate audit reports for compliance and chain of custody

- Bulk import specimens via session-based Excel upload with site locking

- Dedicated report pages with interactive charts (bar, line, pie) for
  inventory, movements, and disposals

- Export data in multiple formats (CSV, Excel, JSON, PDF)

System Requirements
-------------------

- **Browser**: Modern web browser (Chrome 90+, Firefox 88+, Safari 14+,
  Edge 90+)

- **Screen Resolution**: Minimum 1280x720 pixels (1920x1080 recommended)

- **Internet**: Stable internet connection required

- **Authentication**: Email-based account with OTP verification support

Getting Started
===============

Accessing the Application
-------------------------

1. Navigate to the iCCaRE Biobank URL provided by your system
   administrator

2. You will be redirected to the login page if not authenticated

Signing Up
----------

First-time users:
~~~~~~~~~~~~~~~~~

1. Click **"Sign Up"** on the login page

2. Fill in the registration form:

   - First Name and Last Name

   - Email Address (will be your username)

   - Password (must meet security requirements)

   - Confirm Password

3. Click **"Create Account"**

4. Check your email for verification instructions

Logging In
----------

1. Enter your **Email** and **Password**

2. Click **"Sign In"**

3. If OTP (One-Time Password) verification is enabled:

   - Check your email for the verification code

   - Enter the 6-digit code

   - Click **"Verify"**

Navigating the Interface
------------------------

   After successful login, you will see the main interface:

Header (Top Bar)
~~~~~~~~~~~~~~~~

- **Search Bar** — Global search for specimens (Ctrl+K / Cmd+K)

- **Notifications Icon** — View recent alerts and messages

- **Profile Menu** — Access settings, profile, and logout

Sidebar (Left Panel)
~~~~~~~~~~~~~~~~~~~~

- **Dashboard** — Overview and metrics

- **Biospecimen** — Registration, tracking, and bulk upload

- **Attributes** — Configure storage locations and settings

- **User Management** — Manage users and roles (admin only)

- **Reporting** — Analytics, dedicated report pages, and exports

- **Activity Log** — Audit trails and chain of custody

Main Content Area
~~~~~~~~~~~~~~~~~

- Displays the selected module's content

Dashboard
=========

   The Dashboard provides an at-a-glance overview of your biobank
   inventory and activities.

Overview Cards
--------------

   Four key metrics displayed at the top:

- **Total Specimens** — Count of all registered specimens you have
  access to

- **Utilization Rate** — Percentage of occupied storage positions

- **Active Alerts** — Number of pending notifications (expiring samples,
  low temperature alerts)

- **Pending Transfers** — Specimen movements awaiting approval

Freezer Capacity Chart
----------------------

   Visual representation of storage utilization across all freezers:

- Color-coded bars show capacity levels

- Green: < 70% full

- Yellow: 70–90% full

- Red: > 90% full

..

   Click on a freezer bar to view detailed occupancy.

Sample Inventory Trend
----------------------

   Line graph showing specimen count over time:

- Filter by date range (Last 7 days, Last 30 days, Last 90 days, Custom)

- Track inventory growth or reduction

Recent Transfers Table
----------------------

   Displays the most recent specimen movements:

Column Description
~~~~~~~~~~~~~~~~~~

   Sample UUID Unique specimen identifier

   Source Location Origin (Freezer / Rack / Box / Position) Destination
   Location New location

   Movement Type Transfer, Disposal, or Partial Movement Status Pending,
   Approved, Completed, or Rejected Requested By User who submitted the
   request

   Date & Time Timestamp of the request

Actions:
~~~~~~~~

- **Filter** — By status, date range, or location

- **Export** — Download transfer history as CSV or Excel

- **View Details** — Click any row to see complete transfer information

Biospecimen Management
======================

Registration
------------

   Register new specimens into the biobank.

Registering a Single Specimen (4-Step Wizard)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   Registration uses a guided 4-step process. Progress is shown via step
   indicators at the top of the modal. You can navigate forward and
   backward between steps.

1. Navigate to **Biospecimen > Registration**

Click "Register Biospecimen" Step 1 — Basic Information
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Sample Category (select from dropdown)

- Sample Label

- Collection Date (required, YYYY-MM-DD format)

- Collection Time (optional, HH:MM:SS format)

- Researcher Info (required)

- Field Collector Info (required)

Step 2 — Storage Location
~~~~~~~~~~~~~~~~~~~~~~~~~

- Region > Site > Freezer > Rack > Box > Position

- Use cascading dropdowns to navigate the hierarchy

- Position must be a valid, unoccupied grid cell

Step 3 — Metadata
~~~~~~~~~~~~~~~~~

- Initial Volume (optional, positive decimal)

- Current Volume (optional, must be less than or equal to initial
  volume)

- Volume Unit (ml, ul, g, mg, etc.)

- Additional attributes from the selected sample category template

Step 4 — Sample Files
~~~~~~~~~~~~~~~~~~~~~

- Upload file attachments (images, documents)

- Delete uploaded files if needed

- Supports multiple attachments

3. Click **"Register"** on the final step

4. A confirmation message will appear, and the specimen is added to
   inventory

Viewing Registered Specimens
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- **Search** — Use the search bar to find specimens by UUID, subject
  token, or metadata

- **Filter** — Apply filters for category, location, date range, status

- **Sort** — Click column headers to sort by any field

.. _actions-1:

Actions:
~~~~~~~~

- **View** — See complete specimen details

- **Edit** — Update specimen metadata or location

- **Download** — Export specimen data

Tracking (Movement & Disposal)
------------------------------

   Manage specimen movements, partial movements, and disposals through
   approval workflows.

Tab-Based Layout
~~~~~~~~~~~~~~~~

   The Tracking page is organized into three tabs, each showing a count
   badge:

Tab Shows
~~~~~~~~~

   **Pending Movement** Movement requests awaiting approval

   **Pending Disposal** Disposal requests awaiting approval

.. _tab-shows-1:

Tab Shows
~~~~~~~~~

   **Completed Movement** Approved and completed movements

Workflow Overview
~~~~~~~~~~~~~~~~~

   All tracking operations follow a 3-stage workflow:

+-----------------+--------+-----------------+--------+---------+--------------+
|    1. SUBMIT    |    --> |    2. APPROVE / |    --> | 3.      | COMPLETION   |
|    REQUEST      |        |    REJECT       |        | CONFIRM |              |
+=================+========+=================+========+=========+==============+
| (Requester)     |        |    (Approver)   |        | (System | / Requester) |
+-----------------+--------+-----------------+--------+---------+--------------+

Requesting a Specimen Movement
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Navigate to **Biospecimen > Tracking**

2. Click **"Request Movement"**

3. Fill in the request form:

   - **Sample** — Select or enter specimen identifier

   - **Movement Type** — Transfer, Checkout, Return

   - **Source Location** — Current location (auto-filled)

   - **Destination Location** — Select new location

   - **Description** — Describe purpose of movement

   - **Notes** (optional)

4. Click **"Submit Request"**

5. Status changes to **"Pending"** — appears in the Pending Movement tab

Partial Movement
~~~~~~~~~~~~~~~~

   For splitting specimens (e.g., aliquoting):

Click "Request Partial Movement"
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

2. Select movement type:

   - **Position Split** — Move part of sample to a different position

   - **Volume Split** — Divide sample volume

3. Enter split details (new position, volume/quantity)

4. Submit for approval

Disposal Request
~~~~~~~~~~~~~~~~

   To mark specimens as used or disposed:

1. Click **"Request Disposal"** on the Tracking page

2. Fill in:

   - Sample UUID

   - Reason for Disposal (Used in experiment, Degraded, Expired, etc.)

   - Disposal Method (Incineration, Biohazard waste, etc.)

   - Notes

3. Submit for approval

4. Request appears in the **Pending Disposal** tab

Approving / Rejecting Requests
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   **For users with approval permissions:**

1. Navigate to the **Pending Movement** or **Pending Disposal** tab

2. Review the request details:

   - Requester information

   - Specimen details (serial number, label)

   - Source and destination locations

   - Requested date and description

3. Click **"Approve"** or **"Reject"**

4. If rejecting, provide a rejection reason

5. Approved requests move to the **Completed Movement** tab

6. Rejected requests are removed from the pending list

Tracking Table Columns Column Description
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   Sample Serial number or label

   Source Location Current storage location (with pin icon) Destination
   Target location

   Requested Date When the request was submitted Approved Date When
   approved (if applicable) Requested By User who initiated the request
   Description Reason or notes for the movement

   Action Approve / Reject buttons (if you have permission)

Bulk Upload
-----------

   Import multiple specimens at once using a session-based Excel upload
   process with site locking.

How Bulk Upload Works
~~~~~~~~~~~~~~~~~~~~~

   Bulk upload uses a **session-based workflow** that temporarily locks
   a site to prevent conflicts during import. Only one bulk upload
   session can be active per site at a time.

Step-by-Step Process Step 1 — Select Site
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Navigate to **Biospecimen > Bulk Upload**

2. Select a **Site** from the dropdown

3. The system checks if the site is already locked:

   - If locked, you will see who locked it and when the lock expires

   - If unlocked, you can proceed to start a session

Step 2 — Start Session
~~~~~~~~~~~~~~~~~~~~~~

1. Click **"Start Session"**

2. A timed session is created and the site becomes **locked**

3. A **session timer bar** appears at the top showing remaining time

   - The timer turns red when 5 minutes or less remain

   - If the session expires, it is automatically cancelled

Step 3 — Download Template
~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Click **"Download Template"**

2. An Excel file is generated with:

   - Pre-filled dropdown lists for sample category, freezer, rack, box,
     and volume unit

   - Locked columns for site information

   - 16 data columns including collection date, volume, and free fields
     (JSON support)

Step 4 — Fill and Upload Template
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Fill in your specimen data in the downloaded Excel template

2. Save the file (keep it in Excel format)

3. Click **"Upload File"** and select your completed file

4. The system validates all rows **without creating any samples**
   (validation-only phase)

5. Maximum file size: **10 MB Step 5 — Review Validation Results**

..

   If errors are found, they are displayed with row-level detail:

Error types:
~~~~~~~~~~~~

- **Validation errors** — Missing required fields, invalid formats

- **Position conflicts** — A storage position is already occupied

- **Duplicate serial numbers** — Serial number already exists in the
  system

- **Missing references** — Referenced freezer, rack, or box does not
  exist

..

   **Skip options** — You can choose to skip certain error types using
   checkboxes:

- Skip rows with position conflicts

- Skip rows with duplicate serial numbers

- Skip rows with missing references

..

   If no errors are found, proceed directly to confirmation.

Step 6 — Confirm and Import
~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _section-1:

1. Review the validation summary

2. If you enabled skip options, rows with those error types will be
   excluded

3. Click **"Confirm Upload"**

4. The system creates specimens for all valid rows

Step 7 — Success Summary
~~~~~~~~~~~~~~~~~~~~~~~~

   After a successful import, you will see:

- Total rows processed

- Number of successfully created specimens

- Number of failed rows (if any)

- List of created serial numbers

Session Management
~~~~~~~~~~~~~~~~~~

- **Cancel Session** — Click "Cancel Session" at any time to release the
  site lock without importing

- **Session Expiry** — Sessions have a configurable timeout (default
  range: 10–480 minutes). Expired sessions are automatically cancelled.

- **Force Unlock (Admin)** — Administrators can force-unlock a session
  if needed

Attributes (Configuration)
--------------------------

   Configure system settings for specimen management.

Category Types
~~~~~~~~~~~~~~

   Define specimen categories (e.g., Blood, Tissue, DNA, RNA):

1. Navigate to **Attributes > Category Types**

2. Click **"Add Category Type"**

3. Enter:

   - Category Code (e.g., BLD, TIS)

   - Category Name

   - Expiration Days (default shelf life)

   - Description

4. Save

Custom Fields
~~~~~~~~~~~~~

   Add custom metadata fields for specimens:

1. Navigate to **Attributes > Custom Fields**

2. Click **"Create Custom Field"**

3. Configure:

   - Field Name (e.g., "Hemoglobin Level", "Tumor Grade")

   - Field Type (Text, Number, Date, Dropdown)

   - Required (Yes / No)

   - Allowed Values (for dropdown types)

4. Save

..

   Custom fields will appear in the registration form.

Storage Hierarchy
=================

Hierarchy Overview
------------------

   iCCaRE uses a 6-level hierarchical storage structure:

Managing the Hierarchy
----------------------

Regions
~~~~~~~

1. Navigate to **Attributes > Regions**

2. Click **"Add Region"**

3. Enter:

4. Save

Sites
~~~~~

   Region Code (e.g., NE for Northeast) Region Name

   Description

   Status (Active / Inactive)

1. Navigate to **Attributes > Sites**

2. Click **"Add Site"**

3. Fill in:

4. Save

Site Types:
~~~~~~~~~~~

   Site Name

   Region (select from dropdown) Site Type

   Location / Address

   Contact Information (Name, Email, Phone)

Code Type
~~~~~~~~~

   LAB Laboratory

   CLN Clinic

   HSP Hospital

   UNV University

   RSC Research Center

Freezers
~~~~~~~~

1. Navigate to **Attributes > Freezers**

2. Click **"Add Freezer"**

3. Enter:

4. Save

Racks
~~~~~

   Freezer Name / ID

   Site (select from dropdown) Temperature (e.g., -80 degrees C)
   Description

1. Navigate to **Attributes > Racks**

2. Click **"Add Rack"**

3. Fill in:

4. Save

Boxes
~~~~~

   Rack Name / ID

   Freezer (select from dropdown) Capacity (number of boxes) Description

1. Navigate to **Attributes > Boxes**

2. Click **"Add Box"**

3. Configure:

   - Box Name / ID

   - Rack (select from dropdown)

   - Position Template (defines grid layout)

   - Box Type

   - Manufacturer and Model (optional)

4. Save

Position Templates
~~~~~~~~~~~~~~~~~~

   Templates define the grid layout of boxes (e.g., 9x9, 10x10):

1. Navigate to **Attributes > Templates**

2. Click **"Create Template"**

3. Specify:

   - Template Name

   - Rows (e.g., 9)

   - Columns (e.g., 9)

   - Total Positions (auto-calculated: rows x columns)

4. Save

..

   **Common templates:**

+--------------+------------------+--------------------+
| **Template** |    **Positions** |    **Use Case**    |
+==============+==================+====================+
| 9x9          |    81            |    Standard        |
|              |                  |    cryobox         |
+--------------+------------------+--------------------+
| 10x10        |    100           |    Large cryobox   |
+--------------+------------------+--------------------+
| 8x12         |    96            |    Standard        |
|              |                  |    microplate      |
|              |                  |    layout          |
+--------------+------------------+--------------------+

Cascading Filters
-----------------

   When selecting storage locations, dropdowns cascade:

1. Select **Region** — Sites dropdown shows only sites in that region

2. Select **Site** — Freezers dropdown shows only freezers at that site

3. Select **Freezer** — Racks dropdown shows only racks in that freezer

4. Select **Rack** — Boxes dropdown shows only boxes in that rack

5. Select **Box** — Position grid appears showing occupancy

Box Occupancy Grid
------------------

   View and manage specimen placement within boxes:

1. Navigate to a box via **Attributes > Boxes** or through cascading
   filters

2. Visual grid displays:

   - **Green cells** — Empty positions (available)

   - **Red cells** — Occupied positions

   - Hover over occupied positions to see specimen UUID

3. Click on an empty position to register a specimen directly there

User Management
===============

Managing Users
--------------

Creating a New User
~~~~~~~~~~~~~~~~~~~

.. _section-2:

1. Navigate to **User Management > Users**

2. Click **"Create User"**

3. Fill in user details:

   - Email (will be the username)

   - First Name

   - Last Name

   - Password (temporary — user should change on first login)

4. Assign access level (see `Access Control <#access-control>`__):

   - Global Access

   - Regional Access (select regions)

   - Site Access (select sites)

5. Click **"Create User"**

6. User receives activation email

Editing User Information
~~~~~~~~~~~~~~~~~~~~~~~~

1. Click the **Edit** icon next to the user

2. Update fields as needed:

   - Name

   - Email

   - Access level

   - Assigned regions / sites

3. Save changes

Deactivating a User
~~~~~~~~~~~~~~~~~~~

1. Click the **Deactivate** button next to the user

2. Confirm deactivation

3. User can no longer log in (but data is preserved)

Unlocking a Locked Account
~~~~~~~~~~~~~~~~~~~~~~~~~~

   If a user is locked due to failed login attempts:

1. Find the user in the list

2. Click **"Unlock Account"**

3. User can immediately attempt to log in again

Managing Roles
--------------

   Roles define what actions users can perform in the system.

Creating a Role
~~~~~~~~~~~~~~~

1. Navigate to **User Management > Roles**

2. Click **"Create Role"**

3. Configure role properties:

   - **Role Type** — Descriptive name (e.g., "Lab Manager", "Data
     Entry", "Viewer")

   - **Role Function** — Module or feature (e.g., "Specimen Management",
     "User Management")

   - **Function Rights** — CRUD permissions:

     - **C** — Create

     - **R** — Read

     - **U** — Update

     - **D** — Delete

   - **Expiration Date** (optional) — Role auto-revokes on this date

   - **Status** — Enabled / Disabled

4. Save the role

Example Roles:
~~~~~~~~~~~~~~

+------------+----------------+--------------------------+
| **Role     |    **Function  |    **Typical Use Case**  |
| Type**     |    Rights**    |                          |
+============+================+==========================+
| Lab        |    CRUD (all)  |    Full control over     |
| Manager    |                |    specimens             |
+------------+----------------+--------------------------+
| Data Entry |    CR (create, |    Register specimens,   |
| Clerk      |    read only)  |    view data             |
+------------+----------------+--------------------------+
| Auditor    |    R (read     |    View audit logs and   |
|            |    only)       |    reports               |
+------------+----------------+--------------------------+
| Approver   |    RU (read,   |    Approve/reject        |
|            |    update)     |    movement requests     |
+------------+----------------+--------------------------+

..

   **Assigning Roles to Users**

1. Navigate to **User Management > Users**

2. Click **"Assign Role"** next to a user

3. Select one or more roles from the dropdown

4. Click **"Assign"**

5. User immediately gains the permissions

Removing Roles from Users
~~~~~~~~~~~~~~~~~~~~~~~~~

1. Click **"Manage Roles"** next to a user

2. Click the remove icon next to the role

3. Confirm removal

4. Permissions are immediately revoked

Role Expiration
~~~~~~~~~~~~~~~

   Roles with expiration dates automatically revoke on the specified
   date. Users receive a notification before expiration.

Access Control
==============

   iCCaRE implements a hierarchical access control system to ensure
   users only see and manage data they are authorized to access.

Access Levels
-------------

.. _section-3:

+--------------+------------------------+--------------------------------+
| **Access     |    **Scope**           |    **What Users See**          |
| Level**      |                        |                                |
+==============+========================+================================+
| **Global**   |    All regions, sites, |    Entire biobank inventory    |
|              |    and specimens       |    across all locations        |
+--------------+------------------------+--------------------------------+
| **Regional** |    Specific region(s)  |    Only specimens in assigned  |
|              |    and their sites     |    regions                     |
+--------------+------------------------+--------------------------------+
| **Site**     |    Specific site(s)    |    Only specimens at assigned  |
|              |    only                |    sites                       |
+--------------+------------------------+--------------------------------+

2. How Access Level Affects the System

Data Visibility
~~~~~~~~~~~~~~~

- **Specimens:** You only see specimens stored in locations you have
  access to

- **Dropdowns:** Region / Site dropdowns only show your accessible
  locations

- **Dashboard:** Metrics reflect only your accessible data

- **Reports:** Exports include only data within your access scope

Actions by Access Level Global Access Users Can:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Register specimens at any site

- Move specimens between any locations

- Create / edit / delete any storage locations

- Manage all users and roles

- View all audit logs

Regional Access Users Can:
~~~~~~~~~~~~~~~~~~~~~~~~~~

- Register specimens at sites within their assigned regions

- Move specimens within their assigned regions

- View storage locations in their regions

- View audit logs for their regions

Site Access Users Can:
~~~~~~~~~~~~~~~~~~~~~~

- Register specimens at their assigned sites only

- Move specimens within their assigned sites only

- View storage locations at their sites

- View audit logs for their sites

Assigning Access Levels
-----------------------

   System administrators assign access levels when creating or editing
   users:

1. Navigate to **User Management > Users**

2. Click **"Edit"** next to a user

3. Select **Access Level**:

   - **Global** — No further selection needed

   - **Regional** — Select one or more regions

   - **Site** — Select one or more sites

4. Save

Access Level Priority
---------------------

   If a user is assigned multiple access types, the system prioritizes:

   **Global > Regional > Site**

   Example: If a user has both Global and Site access assignments,
   Global takes precedence, and the user has full access.

Permission Flags
----------------

   In addition to access levels, iCCaRE uses **permission flags** to
   control which features, menu items, and action buttons are visible to
   each user. Permission flags follow a fail-closed security model — by
   default, all flags are disabled until explicitly granted by an
   administrator.

How Permission Flags Work
~~~~~~~~~~~~~~~~~~~~~~~~~

- Permission flags are **separate from access levels** — a user needs
  both the right access level (Global/Regional/Site) and the right
  permission flags to perform actions

- They control **menu visibility** (sidebar items appear/disappear),
  **button visibility** (action buttons show/hide), and **page access**
  (unauthorized pages redirect to Dashboard)

- Flags are synced automatically when you log in or when your token
  refreshes

Permission Flag Categories User Management Permissions:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   **Permission Controls**

   Manage Users Visibility of the Users menu and user CRUD Manage Roles
   Visibility of the Roles menu and role CRUD

Biospecimen Permissions:
~~~~~~~~~~~~~~~~~~~~~~~~

   **Permission Controls**

   Manage Samples Access to Registration, Tracking, and Bulk Upload
   pages Manage Storage Access to storage hierarchy management
   (freezers, racks, boxes) Manage Regions Access to region management

Sample-Level Permissions:
~~~~~~~~~~~~~~~~~~~~~~~~~

   **Permission Controls**

Permission Controls
~~~~~~~~~~~~~~~~~~~

   Can Create "Register Biospecimen" button visibility

   Can Read Sample list and detail visibility

   Can Update Edit button on samples

   Can Delete Delete attachments

   Can Request Disposal "Request Disposal" button on Tracking page Can
   Approve Disposal Approve/Reject buttons on disposal requests

   Can Request Tracking "Request Movement" and "Request Partial
   Movement" buttons Can Approve Tracking Approve/Reject buttons on
   movement requests

Reporting & Analytics
=====================

Reports Dashboard
-----------------

   The main Reports page serves as a central hub for data export, report
   scheduling, and alert management.

Dashboard Metrics Card (Top):
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- **Total Records** — Count of all data records

- **New Records (24h)** — Records added in the last 24 hours

- **Data Quality Score** — Percentage indicating data completeness

- **Scope** and **Last Updated** timestamp

Filter & Export Section:
~~~~~~~~~~~~~~~~~~~~~~~~

1. Navigate to **Reporting**

2. Select datasets to include: Samples, Workflows, Freezer Inventory,
   Alerts, Audit Logs, Utilization Metrics, Chain of Custody

3. Optionally filter by Site and Freezer

4. Available actions:

   - **Refresh Dashboard** — Reload dashboard metrics

   - **Export Data** — Opens format selection modal (Excel, CSV, JSON)

   - **Schedule Report** — Configure automated reports

   - **Check & Notify Alerts** — Check threshold-based alerts

   - **Check Utilization** — View freezer capacity (appears when a
     freezer is selected)

..

   **Freezer Utilization Display:** When a freezer is selected, a
   utilization panel shows:

- Total Capacity (units)

- Units Used

- Utilization Percentage — Color-coded: Green (< 50%), Yellow (50–74%),
  Orange (75–89%), Red (90%+)

Sample Inventory Report
-----------------------

   Dedicated report page for viewing specimen status, distribution, and
   volume tracking.

1. Navigate to **Reporting > Sample Inventory**

2. **Filters:** Date range, Region, Site, Status (active, awaiting,
   disposed, depleted)

Table Columns:
~~~~~~~~~~~~~~

   **Column Description**

   Sample ID UUID or serial number

   Site Site name

   Status Color-coded badge (active, awaiting, disposed, depleted)
   Storage Location Formatted as Freezer / Rack / Box

   Initial Volume (mL) Original volume collected Current Volume (mL)
   Remaining volume

   Volume Remaining Visual progress bar with percentage (green >= 50%,
   orange 20–50%, red < 20%) Alert "Low" warning if volume falls below
   20%

Interactive Charts:
~~~~~~~~~~~~~~~~~~~

- **Bar Chart** — Samples by status (active / awaiting / disposed /
  depleted)

- **Pie Chart** — Sample distribution by site

..

   **Export:** Excel, CSV, or JSON

Sample Movements Report
-----------------------

   Dedicated report page consolidating full movements, partial
   movements, and disposals.

1. Navigate to **Reporting > Sample Movements**

2. **Filters:** Date range, Region, Site, Movement type (partial, full,
   disposal)

.. _table-columns-1:

Table Columns:
~~~~~~~~~~~~~~

   **Column Description** Movement ID Request identifier Sample ID
   Serial number or UUID

   Type Color-coded badge — Partial (blue), Full (green), Disposal (red)
   Source Location Origin location hierarchy

   Destination Target location or "Disposed" Requested Date When the
   request was submitted

.. _column-description-1:

Column Description
~~~~~~~~~~~~~~~~~~

   Requested By User who initiated the movement

   Status Pending, Approved, Completed, or Rejected

.. _interactive-charts-1:

Interactive Charts:
~~~~~~~~~~~~~~~~~~~

- **Bar Chart** — Count of movements by type (partial, full, disposal)

- **Line Chart** — Movements over time with separate lines per type

..

   **Export:** Excel, CSV, or JSON

Disposals Report
----------------

   Dedicated report page for tracking specimen disposals by reason,
   volume, and approval status.

1. Navigate to **Reporting > Disposals**

2. **Filters:** Date range, Region, Site, Disposal status (approved,
   pending, completed, rejected)

Summary Cards:
~~~~~~~~~~~~~~

- **Total Disposals** — Overall count

- **Approved** — Includes completed and confirmed

- **Pending Approvals** — Awaiting approval (highlighted in orange)

.. _table-columns-2:

Table Columns:
~~~~~~~~~~~~~~

   **Column Description**

   Disposal ID Request identifier

   Sample ID Serial number or UUID

   Reason Reason for disposal

   Volume (mL) Volume disposed (2 decimal places) Site Site name

   Requested Date Formatted date

   Approved Date Date approved (blank if pending) Requested By User who
   requested disposal Approved By Approver name (or dash if pending)
   Status Color-coded badge

.. _interactive-charts-2:

Interactive Charts:
~~~~~~~~~~~~~~~~~~~

- **Pie Chart** — Disposals by reason (color-coded breakdown)

- **Line Chart** — Disposal volume over time

..

   **Export:** Excel, CSV, or JSON

Freezer Utilization Report
--------------------------

   Monitor storage capacity:

1. Navigate to **Reporting > Utilization** or select a freezer on the
   Reports Dashboard

2. View utilization by Freezer, Rack, or Box

3. Color-coded indicators:

   - Green: < 50% full

   - Yellow: 50–74% full

   - Orange: 75–89% full

   - Red: 90%+ full (action recommended) Export utilization data as CSV
     or Excel.

Data Export
-----------

   Export specimen data for external analysis:

1. Navigate to **Reporting**

2. Select datasets to export (Samples, Workflows, Freezer Inventory,
   etc.)

3. Optionally filter by Site and Freezer

4. Click **"Export Data"**

5. Choose format: **Excel**, **CSV**, or **JSON**

6. File downloads to your computer

Scheduling Reports
------------------

   Automate regular reports:

1. Navigate to **Reporting**

2. Click **"Schedule Report"**

3. Configure:

   - Report Name

   - Frequency (Daily, Weekly, Monthly)

   - Recipient Emails

   - Recipient Roles

4. Click **"Schedule"**

Alerts & Notifications
----------------------

   Configure threshold-based alerts:

1. Navigate to **Reporting**

2. Click **"Check & Notify Alerts"**

3. Fill in:

   - Item Name

   - Units

   - Threshold Value

   - Current Value

   - Admin Notes

4. Click **"Check & Notify"**

..

   If the threshold is exceeded, an alert is triggered and a
   notification is sent. The alert response shows the Alert ID, item
   details, current vs. threshold values, and notification status.

Activity Log & Audit Trail
==========================

Audit Logs
----------

   Complete record of all system activities for compliance and
   troubleshooting.

Viewing Audit Logs
~~~~~~~~~~~~~~~~~~

1. Navigate to **Activity Log > Audit Logs**

2. The table displays:

.. _column-description-2:

Column Description
~~~~~~~~~~~~~~~~~~

   Timestamp Date and time of the action User Who performed the action

   Action Type CREATE, UPDATE, DELETE, LOGIN, APPROVE, REJECT

   Affected Entity Specimen UUID, User ID, Location ID Details
   Description of the action

   IP Address Origin of the request

Filtering Audit Logs
~~~~~~~~~~~~~~~~~~~~

   Use filters to narrow results:

- **User** — Select specific user(s)

- **Action Type** — CREATE, UPDATE, DELETE, LOGIN, LOGOUT, APPROVE,
  REJECT

- **Date Range** — From / To dates

- **Entity Type** — Specimen, User, Location, Role

- **Search** — Keyword search in details

Exporting Audit Logs
~~~~~~~~~~~~~~~~~~~~

1. Apply desired filters

2. Click **"Export Audit Logs"**

3. Select format: **CSV**, **PDF**, or **JSON**

4. Download file

Chain of Custody
----------------

   Track complete movement history for individual specimens.

Viewing Chain of Custody
~~~~~~~~~~~~~~~~~~~~~~~~

1. Navigate to **Activity Log > Chain of Custody**

2. Search for a specimen by UUID

3. View complete custody timeline:

   - **RECEIVED** — Initial registration

   - **STORED** — Placed in storage location

   - **TRANSFERRED** — Moved between locations

   - **ANALYZED** — Used in experiment or test

   - **DISPOSED** — End of lifecycle Each event includes:

- Timestamp

- User responsible

- Source and destination

- Reason / notes

- Digital signature (if configured)

Generating Custody Reports
~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Enter specimen UUID

Click "Generate Custody Report"
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

3. Report includes:

   - Specimen details

   - Complete custody history

   - All locations visited

   - All users who handled the specimen

   - Digital signatures

4. Export as PDF for documentation

Notifications
=============

   Stay informed about important system events and alerts.

Viewing Notifications
---------------------

1. Click the **Notification Bell** icon in the header

2. Notification panel opens, showing:

   - Notification message

   - Timestamp

   - Priority level

   - Read / Unread status

Notification Types
------------------

- **Inventory Alerts** — Low stock, high utilization, expiring specimens

- **Transfer Notifications** — Movement requests pending your approval

- **System Alerts** — Temperature warnings, system maintenance

- **User Notifications** — Account changes, role assignments

Notification Priorities
-----------------------

Priority Meaning
~~~~~~~~~~~~~~~~

   Normal Informational, no immediate action required High Attention
   needed, action recommended Urgent Immediate action required (critical
   alert)

Managing Notifications
----------------------

- **Mark as Read** — Click on a notification to mark it as read, or
  click **"Mark All as Read"**

- **Filter** — Toggle between All, Unread Only, or filter by type

- **Unread Count** — Red badge on notification icon shows count of
  unread notifications

Profile & Settings
==================

Personal Information
--------------------

   Update your profile details:

1. Click your **Profile Icon** in the header

2. Select **"Profile"**

3. Edit fields:

   - First Name

   - Last Name

   - Phone Number

4. Click **"Save Changes"**

Security & Authentication
-------------------------

Changing Your Password
~~~~~~~~~~~~~~~~~~~~~~

1. Navigate to **Profile > Security**

2. Click **"Change Password"**

3. Enter:

..

   |image1| Current Password

   |image2| New Password (must meet requirements)

   |image3| Confirm New Password

Click "Update Password" Password Requirements:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Minimum 8 characters

- At least one uppercase letter

- At least one lowercase letter

- At least one number

- At least one special character

Two-Factor Authentication (OTP)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   Enable OTP for enhanced security:

1. Navigate to **Profile > Security**

2. Toggle **"Enable OTP Verification"**

3. On next login, you will receive a verification code via email

User Preferences
----------------

   Customize your experience:

1. Navigate to **Profile > Preferences**

2. Configure:

   - **Timezone** — Select your local timezone for accurate timestamps

   - **Language** — Select interface language (if available)

   - **Notifications** — Enable / disable email notifications

   - **Theme** — Light or Dark mode

3. Click **"Save Preferences"**

.. _data-export-1:

Data Export
===========

Available Export Formats
------------------------

+------------+-----------------------------+------------------------+
| **Format** |    **Use Case**             |    **Available For**   |
+============+=============================+========================+
| **CSV**    |    Data processing, Excel   |    Specimens,          |
|            |    import, analysis         |    Transfers, Audit    |
|            |                             |    Logs                |
+------------+-----------------------------+------------------------+
| **Excel**  |    Pre-formatted            |    Specimens, Reports  |
|            |    spreadsheets with        |                        |
|            |    styling                  |                        |
+------------+-----------------------------+------------------------+
| **JSON**   |    API integration, data    |    Specimens, Audit    |
|            |    pipelines                |    Logs                |
+------------+-----------------------------+------------------------+
| **PDF**    |    Documentation, printed   |    Audit Logs, Custody |
|            |    reports                  |    Reports             |
+------------+-----------------------------+------------------------+

2. Where Export is Available

- **Biospecimen Registration** — Export all registered specimens with
  metadata and custom fields

- **Transfer History** — Export tracking requests with source,
  destination, and approval details

- **Audit Logs** — Export filtered audit records with user actions and
  timestamps

- **Reports** — Dashboard data, utilization reports, and scheduled
  report outputs

- **Chain of Custody** — PDF custody reports for individual specimens

Export Process
--------------

1. Navigate to the desired module (Registration, Tracking, Audit, etc.)

2. Apply filters if needed (date range, status, location)

3. Click the **"Export"** button

4. Select format (CSV, Excel, JSON, or PDF)

5. File downloads to your browser's default download folder

Keyboard Shortcuts & Tips
=========================

Keyboard Shortcuts
------------------

Shortcut Action
~~~~~~~~~~~~~~~

   Ctrl+K / Cmd+K Open global search

   Esc Close modal / dialog

Navigation Tips
---------------

- **Quick Search** — Use the global search bar (Ctrl+K) to find
  specimens by UUID or subject token. Results update as you type.

- **Copy to Clipboard** — Click the copy icon next to UUIDs or IDs to
  copy to clipboard for sharing or pasting into other systems.

- **Breadcrumb Navigation** — Use breadcrumbs at the top of the page to
  navigate back to parent pages.

Table Tips
----------

- **Sorting** — Click any column header to sort ascending; click again
  for descending

- **Pagination** — Use page controls at the bottom of tables; adjust
  "Items per page" for larger views (10, 25, 50, 100)

- **Bulk Selection** — Use the checkbox in the header to select all
  visible items

Form Tips
---------

- **Required Fields** — Marked with a red asterisk (\*). The form will
  not submit until all are filled.

- **Validation** — Real-time validation shows errors as you type. Red
  borders indicate invalid input.

- **Autocomplete** — Dropdowns with search support: start typing to
  filter options.

- **Date Pickers** — Click the calendar icon or type the date in
  YYYY-MM-DD format.

Productivity Tips
-----------------

- **Use Filters First** — Apply filters before exporting to reduce file
  size

- **Bookmark Pages** — Save frequently used pages for quick access

- **Check Notifications Daily** — Stay on top of pending approvals and
  alerts

- **Verify Before Bulk Upload** — Test with 5–10 rows first, then upload
  the full dataset

- **Schedule Reports** — Automate recurring reports instead of exporting
  manually

- **Use Templates** — Create position templates for reusable box layouts

- **Enable OTP** — Add two-factor authentication for enhanced security

Support & Help
==============

Getting Help
------------

- **System Administrator** — Contact your organization's biobank
  administrator for account issues, access requests, or permissions

- **Technical Support** — Email your IT support team for login issues,
  password resets, or technical errors

- **User Guide** — Refer to this guide for step-by-step instructions

Frequently Asked Questions
--------------------------

   **Q: I forgot my password. How do I reset it?** A: Click "Forgot
   Password" on the login page and follow the email instructions.
   Contact your administrator if the email does not arrive.

   **Q: I cannot see certain regions or sites in dropdowns. Why?** A:
   Your access level restricts which locations you can see. Contact your
   administrator to request access to additional regions or sites.

   **Q: My account is locked. What should I do?** A: After multiple
   failed login attempts, accounts are temporarily locked. Contact your
   administrator to unlock your account.

   **Q: Why can I not approve a transfer request?** A: You need approval
   permissions (assigned via roles). Contact your administrator to
   request the appropriate role.

   **Q: My bulk upload failed. What went wrong?** A: Check the
   validation results for row-level errors. Common issues include
   missing required fields, invalid locations, duplicate serial numbers,
   position conflicts, or incorrect date formats. You can use the skip
   checkboxes to exclude rows with certain error types and re-submit.

   **Q: The site is locked and I cannot register specimens. What do I
   do?** A: Another user has an active bulk upload session for that
   site. Wait for the session to complete or expire, or ask an
   administrator to force-unlock the session.

   **Q: I cannot see certain buttons (Register, Request Movement, etc.).
   Why?** A: Your account does not have the required permission flag for
   that action. Contact your administrator to request the appropriate
   permission.

   **Q: Can I undo a disposal?** A: No. Disposals are permanent once
   confirmed. If you accidentally disposed of a specimen, contact your
   administrator immediately.

Appendix: Glossary
==================

.. _section-4:

Term Definition
~~~~~~~~~~~~~~~

   **Access Level** Permission tier (Global, Regional, Site) determining
   what data a user can see and manage

   **Aliquot** A portion of a specimen divided for separate storage or
   testing

   **Audit Log** Immutable record of all system activities for
   compliance and traceability **Biospecimen** A biological sample
   collected from a subject for research or clinical purposes **Box**
   Storage container with a grid layout (e.g., 9x9, 10x10) for holding
   specimens **Category Type** Classification of specimens (e.g., Blood,
   Tissue, DNA, RNA)

   **Chain of Custody** Documented record of specimen handling,
   movement, and storage

   **Custom Field** User-defined metadata attribute for specimens

   **Disposal** Permanent removal of a specimen from inventory (used,
   degraded, or destroyed)

   **Freezer** Temperature-controlled storage unit (e.g., -20C, -80C,
   liquid nitrogen)

   **OTP** One-Time Password — temporary verification code sent via
   email for two-factor authentication

   **Partial Movement** Splitting a specimen into multiple portions or
   aliquots

   **Position** Individual cell in a box grid where a specimen is stored

   **Rack** Shelf or compartment within a freezer holding multiple boxes

   **Region** Geographic area containing one or more sites

   **Role** Set of permissions defining what actions a user can perform

   **Site** Physical location (laboratory, clinic, hospital, university,
   research center)

   **Subject** Individual from whom a specimen was collected

   **Template** Grid layout definition for boxes (rows x columns)

   **Permission Flag** Fine-grained control determining which features,
   buttons, and menu items a user can access

Session (Bulk Upload)
~~~~~~~~~~~~~~~~~~~~~

   A timed, site-locked period during which bulk specimen import occurs

   **Site Lock** Temporary lock on a site during an active bulk upload
   session, preventing individual registration

   **Tracking** Recording and approving specimen movements between
   storage locations

   **UUID** Universally Unique Identifier for specimens

   **Utilization Rate** Percentage of occupied storage positions

   **Document Version:** 1.1 **Last Updated:** February 25, 2026
   **iCCaRE Biobank System**

.. |image1| image:: media/image30.png
.. |image2| image:: media/image31.png
.. |image3| image:: media/image32.png
