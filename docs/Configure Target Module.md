---
layout: default
title: Configure Target Module
nav order: 4
---
# Configure Target Module
{: .no_toc }

---

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

---

## Overview

This guide will show you how to configure the target module (Primary and/or Secondary) and create/update a record in a specified module when an email is received.

## Prerequisites

Make sure you’ve successfully installed and configured SuiteCRM Email to Anything.

- **Installation:** For detailed instructions on how to install the software, please refer to our Installation Guide.
- **Inbound Email Configuration:** After installation, you'll need to configure the product to meet your specific needs. Our Inbound Email Configuration Guide provides step-by-step instructions for this process.

## Email to Anything Receiver Setting

{: .note }
An Email to Anything receiver is automatically generated e.g. AutoMatically Generated Receiver For *inboundemail@yourcompany.com*

Follow the steps given below to create an email receiver setting and set up target module(s).

1. Go to Administration Panel and scroll to SuiteCRM Email to Anything section.
1. Click **Step 4**. This will take you to the Email to Anything Receiver settings.
1. Click **Create Receiver Setting** on the left navigation panel.
1. This is the Basic Configuration of the receiver.
    - **Receiver Name:** Give a befitting name to the receiver setting.
    - **Primary Target:** Select the primary target module in which you want to create records and save data extracted from email. Primary module examples are Leads, Contacts, Accounts, etc.
    - **Secondary Target:** Select the secondary target module in which you want to create records. The secondary target could be in relationship with the primary target for example Meetings, Calls, Notes, etc.

    {: .important }
    Choose `Home` in Secondary Target if you do not want to create records in secondary modules.

    - **Target Email Address:** This receiver setting will apply to the inbound email address mentioned here.
    - **Field value separator:** This is a key value separator e.g. Name:: John. By default, it’s a double-colon (::), but you can change it as needed.
    - **Status:** You can active or inactive the receiver using the status dropdown.
1. Click **Save** when all fields are filled.

{: .highlight }
>**Tip:** You can create multiple receiver settings to create records in different target modules.

## Example

Imagine you receive an email containing contact information, and you want to automatically create a new contact record in SuiteCRM based on the data in the email.

### Sample Email
{: .no_toc }

---

<dl>
  <dt>First Name</dt>
  <dd>John</dd>
  <dt>Last Name</dt>
  <dd>Doe</dd>
  <dt>Office Phone</dt>
  <dd>8999999999</dd>
  <dt>Job Title</dt>
  <dd>Editor</dd>
  <dt>Department</dt>
  <dd>Publication</dd>
  <dt>Email Address</dt>
  <dd>johndoe@email.com</dd>
  <dt>Website</dt>
  <dd>editor.com</dd>
</dl>

---

### Extraction Process
{: .no_toc }

Our SuiteCRM Email to Anything plugin scans the email body for key-value pairs and identifies the contact details using predefined patterns. In this case, it extracts "First Name," “Last Name”, “Office Phone”, “Job Title”, “Department”, “Email Address”, and “Website” as keys.

### Record Creation
{: .no_toc }

The extracted data is used to create a new contact record in SuiteCRM. The "Name” “Office Phone”, “Job Title”, “Department”, “Email Address”, and “Website” fields in SuiteCRM are populated with the respective values extracted from the email.

This example demonstrates the process of extracting contact information from an email and using it to create a new contact record in SuiteCRM.

## Additional Resources

- Installation guide
- Inbound email configuration guide
