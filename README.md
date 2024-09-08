# Create Kubernetes Cluster on Google Kubernetes Engine

This guide outlines the steps to create a Kubernetes cluster on Google Kubernetes Engine (GKE) using the Google Cloud Console.

## Prerequisites
- A Google Cloud account
- Billing enabled for your Google Cloud project

## Steps

### 1. Access the Google Cloud Console
Sign in to the Google Cloud Console: [Google Cloud Console](https://console.cloud.google.com/)

### 2. Create a New Project
1. In the Google Cloud Console, go to the **Manage Resources** page.
   - [Go to Manage Resources](https://console.cloud.google.com/iam-admin/projects)
   
2. Click the **Create Project** button.
   
   
   
3. In the **New Project** window, name the project `saleor-cluster`. The project name must be between 4 and 30 characters.



4. In the **Location** box, specify the parent organization or folder resource if applicable. Otherwise, you can create the project as the top-level resource.

5. Click **Create**.

![Create Project Button](images/creating%20cluster.png)

### 3. Enable Required APIs
1. Enable the **Google Kubernetes Engine** and **Artifact Registry** APIs:
   - [Enable the APIs](https://console.cloud.google.com/flows/enableapi?apiid=container.googleapis.com,artifactregistry.googleapis.com)

### 4. Launch Cloud Shell
1. In the upper-right corner of the console, click the **Activate Cloud Shell** button.
   


2. This will launch a Cloud Shell session, giving you access to the Google Cloud CLI and `kubectl`, the primary command-line tools for managing your Google Cloud resources and Kubernetes clusters.
   
   ![Activate Cloud Shell](images/entry%20generated%20for%20cluster.png)

### 5. Set the Default Project
1. In the Cloud Shell, set your default project by running the following command:
   ```bash
   gcloud config set project isec6000-SecureDevOps

### Authorize Cloud Shell
If this is your first time using Cloud Shell, authorize it when prompted.

---

### 6. Set Default Compute Zone
Set the default compute zone where your clusters and resources will be physically located. Run the following command in Cloud Shell:

```bash
gcloud config set compute/zone us-central1-a
```

> **Note:** You can change `us-central1-a` to any other zone of your preference.
   ![Activate Cloud Shell](images/cluster%20creater.png)
---

### 7. Create Kubernetes Cluster
1. From the navigation menu, select **Kubernetes Engine**, then click **Clusters**.

2. Configure your cluster settings (name, location, node pool configuration).

3. Click **Create** to provision the GKE cluster.

4. Wait for the cluster `isec6000-cluster` to be created.

---

### 8. Install and Configure `kubectl`
1. After the cluster is created, click **Connect** in the cluster actions.

2. In the dialog box that appears, click **Run in Cloud Shell** to automatically configure `kubectl` command-line access.

---

### Conclusion
You have successfully created a Kubernetes cluster on GKE and configured `kubectl` for managing the cluster. You can now deploy applications to your cluster using the `kubectl` command-line tool.

---