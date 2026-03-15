# 🎥[Watch me Building and Hosting a Static Website](https://www.loom.com/share/db9da8a16f0d451ca61183cf48bb5839)

# Building and Hosting a Static Website with Azure Storage

This guide walks through the process of configuring an Azure Storage Account to host a static website.

---

## Step 1: Sign in to the Azure Portal
![alt text](https://github.com/glenpagesr-dev/Building-and-Hosting-a-Static-Website-on-Azure/blob/main/sign%20in%20to%20the%20Azure%20Portal.png)
1. Navigate to the **Azure Portal** 
2. Sign in using your Azure account credentials.
3. From the Azure home page, locate the search bar at the top.

---

## Step 2: Create a Storage Account
![alt text](https://github.com/glenpagesr-dev/Building-and-Hosting-a-Static-Website-on-Azure/blob/main/create%20storage%20account.png)

1. In the search bar, type **Storage accounts** and select it.
2. Click **Create**.
3. Under the **Basics** tab, configure the following:
   - **Subscription**: Select your active subscription.
   - **Resource group**: Create a new resource group or select an existing one.
   - **Storage account name**: Enter a globally unique name (lowercase letters and numbers only).
   - **Region**: Choose a region closest to you.
   - **Performance**: Select **Standard**.
   - **Redundancy**: Select **Locally-redundant storage (LRS)**.

4. Click **Review + create**, then click **Create**.

---

## Step 3: Enable Static Website Hosting
![alt text](https://github.com/glenpagesr-dev/Building-and-Hosting-a-Static-Website-on-Azure/blob/main/enable%20website.png)

1. Once the storage account is deployed, open it.
2. In the left-hand menu, scroll to **Data management**.
3. Select **Static website**.
4. Toggle **Static website** to **Enabled**.
5. Enter the following:
   - **Index document name**: `index.html`
   - **Error document path**: `404.html`
6. Click **Save**.

> **Note:** Enabling this feature automatically creates a container named `$web`.

---

## Step 4: Upload Website Files to the `$web` Container
![alt text](https://github.com/glenpagesr-dev/Building-and-Hosting-a-Static-Website-on-Azure/blob/main/upload%20Blob.png)

1. From the storage account menu, select **Containers**.
2. Open the **$web** container.
3. Click **Upload**.
4. Upload your static website files:
   - `index.html`
   - `404.html` (optional)
   - Any supporting files (CSS, images, JavaScript)
5. Click **Upload** to complete the process.

---

## Step 5: Verify Public Access Settings
![alt text](https://github.com/glenpagesr-dev/Building-and-Hosting-a-Static-Website-on-Azure/blob/main/Allow%20Blob%20Anonymous%20Access.png)

1. In the storage account menu, select **Configuration**.
2. Ensure **Allow Blob anonymous access** is set to **Enabled**.
3. Click **Save** if changes are made.

> **Important:** Static websites require anonymous read access to function correctly.

---

## Step 6: Access the Static Website
![alt text](https://github.com/glenpagesr-dev/Building-and-Hosting-a-Static-Website-on-Azure/blob/main/Web%20Site.png)

1. Return to **Static website** under **Data management**.
2. Copy the **Primary endpoint** URL.
3. Paste the URL into a web browser.

You should now see your static website live and accessible from the internet.

---

## Next Steps: Enhancements and Security

- Configure a **custom domain** using Azure DNS.
- Enable **HTTPS** using Azure-managed certificates.
- Integrate **Azure CDN** for improved performance.
- Use **Azure DevOps or GitHub Actions** to automate deployments.

This completes the process of hosting a static website on Azure using Azure Storage.
