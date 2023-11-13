---
layout: default
title: Create and Update Rules
nav_order: 8
---
# Create and Update Rules
{: .no_toc }

<details open markdown="block">
  <summary>
        Table of Contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

---

## Overview

The Create/Update Rule feature decides whether to create a new record or update an existing one. It controls how we manage email data, ensuring that every information goes to the right spot in our system, whether creating a new record or updating an existing one.

## Default Record Creation Process

Here is the default record creation process. When no switches are enabled, the following create/update rule will apply. Check the decision tree methodology below to understand the complete process.

1. Parse Email Data: Start by parsing the data from the email, extracting relevant information, such as name, phone number, and email address.
1. Check for Duplicate Records:
    1. If No Duplicate Records Exist:
        1. Create New Record: If there are no existing records with the same phone number or email address, create a new record in the system using the parsed data.
    1. If Duplicate Records Exist:
        1. Compare with Existing Records:
            1. If Matching Phone Number or Email Address Found:
                1. Update Existing Record: If a record with a matching phone number or email address is found, update that existing record with the parsed data.
            1. If No Matching Phone Number or Email Address:
                1. Create New Record: If no matching records are found, create a new record in the system with the parsed data.

## Always Create New Records

In this case, the plugin will create a new record for every new incoming email.

## Never Update Record

In this case, the plugin will neither update the existing record nor create a new record even if duplicate records are found based on the email address or phone number. Instead, it will attach the incoming email to the history subpanel.

## Never Create New Records (Primary Module)

The plugin will neither create a new record nor update the existing record in the primary module only.

## Never Create New Records (Secondary Module)

The plugin will neither create a new record nor update the existing record in the secondary module only.

## Follow Steps to Enable

1. Go to the Administration panel, in the SuiteCRM Email to Anything section select **View all receivers**.
1. Select an Email to Anything Receiver setting from the list view.
1. Click **Show All Switches**.
1. You will find all options in the Create/Update Rules panel.
