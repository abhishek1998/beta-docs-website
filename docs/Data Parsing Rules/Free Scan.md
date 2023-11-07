---
layout: default
title: Free Scan
parent: Data Parsing Rules
nav_order: 2
---

# Free Scan
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---
## Overview

Enable this switch if the email format doesn’t have any key-value pairs or unstructured emails. If the free scan is enabled, information like name, email address, website, phone number, and designation (CEO, Co-founder, CTO, etc.) will automatically be extracted from emails.

## Prerequisites

System administrator access to the SuiteCRM

## Steps Need to Follow

1. Go to the Administration panel.
1. Navigate to the Email to Anything by Outright Store section and select **View all receiver settings**.
1. Click on the pencil icon (✎) to edit the E2A receiver setting.
1. Click on **Show all switches**.
1. In **Data Parsing Rules** section, enable the **Free Scan** switch.

## Example of Free Scan

In this email sample, the name and email address will be extracted from the sender’s data. Other information like websites and phone numbers will be extracted from the body.

The plugin will also extract the designations like CEO, founder, CTO, etc. (You can change it as per requirements.)
