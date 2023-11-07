---
layout: default
title: New Line
parent: Data Parsing Rules
nav_order: 1
---

# New Line
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Overview

Enable this switch if the email format has a key and its value in separate consecutive lines. Check the example below that shows an email format with the key (Name) in one line and the value (Elon Musk) in the next line.

## Prerequisites

System administrator access to the SuiteCRM

## Steps Need to Follow

1. Go to the Administration panel.
1. Navigate to the Email to Anything by Outright Store section and select **View all receiver settings**.
1. Click on the pencil icon (✎) to edit the E2A receiver setting.
1. Click **Show all switches**.
1. In **Data Parsing Rules** section, enable the **Next Line** switch.

## Example of Next-Line Email

This example email shows the data structure of the incoming email body.

```text
Name
Elon Musk

Email Address
elonmusk@tesla.com

Office Phone
+1545668466

Zip
22939

Location
Dallas, Texas

Preferred Contact Method
Email

Product
Electric Spaceship

Model
Model X

Price
$5,000,000.00
```

## Result

The plugin will extract the data and create a record in the selected target module.
