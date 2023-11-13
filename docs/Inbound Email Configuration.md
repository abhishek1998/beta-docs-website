---
layout: default
title: Inbound Email Configuration
nav_order: 3
---

# Inbound Email Configuration
{: .no_toc }

---

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

This document guides you through the inbound email configuration of SuiteCRM Email to Anything using Gmail API and Google Cloud Pub/Sub.

## Initial Configuration in Google Cloud

- Enable Gmail API
- Configure Consent Screen
- Configure OAuth 2.0 Client
- Create Pub/Sub Topic and Subscription

### Enable Gmail API

{: .important}
You need to Sign up/Log in with the same Gmail address that you will be using for Email to Anything.

1. Go to the [Google Cloud Console](https://console.cloud.google.com/)
1. Create a new project. For this, on the top left, click the navigation menu  **☰ > IAM & Admin > Create a project**.

    ![New Project](../../assets/images/new-project.png)
1. Give a project name and ID, and select the organization. Click **Create**.
1. Go to Menu **☰ > APIs & Services > Library**.
1. In the search bar, type and select **Gmail API**.

    ![Enable Gmail API](../../assets/images/enable-gmail-api.png)
1. Click **Enable**.

### Configure Consent Screen

{: .note}
If you are configuring OAuth 2.0 Client for the first time, you must configure Consent Screen first.

1. Go to the Navigation Menu **☰ > APIs & Services > Credentials**.
1. Click the **Configure Consent Screen** on the right.
1. Next, choose whether the app users are internal or external.
        <!--- ![User Type](../../assets/images/user-type.png) --->
    1. Select **Internal** If you use the organization’s email address(es).
    1. Select **External** if you use a generic Gmail address(es). (In this case, you need to verify your application.)
1. Next, provide the app name, users will see it on the consent screen.
1. Provide required information i.e. **User support email** and **Developer contact information**. Click **Save and continue**.
1. For internal organization users, the scopes are not listed. Click **Save and continue**, and your consent screen is configured successfully.

### Configure OAuth 2.0 Client

1. Go to the [Google Cloud Platform Console](https://console.cloud.google.com/welcome)
1. Select the same project in which you’ve enabled Gmail API.
1. Click the Navigation Menu **☰ > APIs & Services > Credentials**.
1. Click **+ Create Credentials** and then select **OAuth client ID**.
1. Select the application type as a Web application.
1. Give a name to the OAuth 2.0 client.
1. Click **Create** at the bottom.

    ![Client ID and Client Secret](../../assets/images/client-id-secret.png)
1. Copy **Client ID** and **Client Secret** from the pop-up dialog.

{: .highlight }
>**Tip:** Please copy Client ID and Client Secret, you will need both in SuiteCRM configuration.

### Create Pub/Sub Topic and Subscription

1. Go to Google Cloud Console and open the [pub/sub topic](https://console.cloud.google.com/cloudpubsub/topic) page.
1. Click **Create Topic**.
1. In the Topic ID, provide a suitable topic name then click **Create**.
1. In the info panel on the right, click the **Add Principal**.
    ![Add Principals](../../assets/images/add-principals.png)
1. In the **New Principals**, type and select `allUsers`.
1. Again in the New Principals box, type and select `gmail-api-push@system.gserviceaccount.com`.
1. In the **Assign Roles**, choose **Pub/Sub > Pub/Sub Admin**.
1. Click **Save** at the bottom.

## Inbound Email Configuration in SuiteCRM

1. Go to the Administration Panel.
1. In the Email to Anything by Outright Store section, click Step 2 to **Create New Inbound Email Settings**.

    ![Inbound Email Setting](../../assets/images/inbound-setting.png)
1. In **Email Address as Archiver**, enter the email address whose emails you want to retrieve.
1. **Email 2 Anything Manager** will auto-fill.
1. Provide the **Client ID** and **Client Secret**, you’ll get them from the OAuth 2.0 Client.
1. Select the **Status** Checkbox to activate the inbound setting.
1. Provide **Pub/Sub Topic Name**, you’ll get it from the Google Cloud PUB/SUB section.
1. Click **Save**.
1. Click on the **Copy Redirect URL** button. This will get you a redirect URL that needs to be added to the OAuth Client.
    1. Go to Google Cloud Console then **Navigation Menu>APIs & Services>Credentials**.
    1. Select the OAuth 2.0 Client ID that you created.

        ![Add Redirect URI](../../assets/images/add-redirect-url.png)
    1. In the Authorized redirect URIs section, click **Add URI** and paste the redirect URL.
1. Click on the **Copy Webhook URL** button. This will get you a Webhook URL that needs to be added to the Cloud Subscription.
    1. Go to Google Cloud Console then Navigation **Menu>Pub/Sub>Subscriptions**.
    1. Click on the subscription you created earlier.
    1. Click on the **edit** at the top.
    1. Change **Delivery Type** to **Push**.

        ![Add Webhook](../../assets/images/add-webhook.png)
    1. In the **Endpoint URL**, paste the webhook URL that you copied.
    1. Click **Update** at the bottom.
1. In SuiteCRM, Click **Sign in with Google** and log in with your Gmail account.
1. Allow the required permissions.
1. Select which email folder/label you would like Email to Anything to read.

You have now successfully configured your inbound email address.

The next step is to configure the target module in [Email to Anything Receiver setting](https://abhishek1998.github.io/beta-docs-website/docs/Configure%20Target%20Module/).