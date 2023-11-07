---
layout: default
title: Fuzzy Matching
parent: Data Parsing Rules
nav_order: 3
---

# Fuzzy Matching
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Overview

This helps to find approximate matching even when the values in the email body are misspelled or omitted.

## Prerequisites
- System administrator access to the SuiteCRM

## Steps Need to Follow

1. Go to the Administration panel.
1. Navigate to the Email to Anything by Outright Store section and select **View all receiver settings**.
1. Click on the pencil icon (✎) to edit the E2A receiver setting.
1. Click **Show all switches**.
1. In **Data Parsing Rules** section, enable the Fuzzy Detection switch.

## Example of Fuzzy Detection

In this example, the primary module is Meetings and the secondary module is Accounts.
After we send this email, a meeting will be created and the account will be attached to the meeting.

```text
Subject:: Let's meet online
Start Date::  09/15/23 01:15
Location:: Virtual Meeting
Related to:: Accounts, Stefen
```

## Result

A meeting is created and an account is attached to the meeting even though the spelling is different.
