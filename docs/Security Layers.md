---
layout: default
title: Security Layers
nav order: 13
---

# Security Layers
{: .no_toc }

---

<details open markdown="block">
  <summary>
        Table of Contents
  </summary>
  {: .text-delta}
- TOC
{:toc}
</details>

---

## Overview

You will get 2 security layers with Email to Anything to keep your SuiteCRM secure from unwanted, harmful, spam, and unauthorized emails. You can access the options from the left-side navigation panel.

## Layer 1: Authorized Senders

### 1.1 Authorized Domain

You can enter an email domain e.g. `outrighcrm.com`. SuiteCRM Email to Anything will only process emails sent from `jane@outrighcrm.com`, `steve@outrighcrm.com`, etc. In this case, emails by other senders outside this domain will not be authorized to parse in SuiteCRM.

### 1.2 Authorized Email

Enter an email address like `elon@example.com`. SuiteCRM Email to Anything will only process emails sent from `elon@example.com`. In this case, emails sent by other senders will not create records in SuiteCRM.

### How to enable authorized email address and email domain

1. Click **Authorized Domains** on the left.
1. Click **Create**.
1. In **Only Allow Email or Domains**, enter the email address/domain you want to allow to create records.
1. Click **Save**.

## Layer 2: Spam Keyword Filters

### 2.1 Spam Keyword in Email Body

You can filter emails based on spam keywords. For example, if the email body consists of the word “Confidential” then you can add it here. After that, SuiteCRM Email to Anything will not parse emails with the word  “Confidential” in their body.

### 2.2 Spam Keyword in Subject

You can filter emails based on spam keywords. For example, if the email subject consists of the word “Confidential” then you can add it here. SuiteCRM Email to Anything will not parse emails with the word  “Confidential” in their subject.

### How to Enable Spam Keyword Detector for Email Body and Subject

1. Click **Spam Detector Keywords** on the left.
1. Click **Create**.
1. Enter the keyword in the **Spam keyword in Email Body**.
1. Click **Save**.

## Spam Notices

You can see all filtered emails containing Spam keywords in the email body and the subject will appear in this module.
