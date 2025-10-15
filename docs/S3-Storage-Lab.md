# AWS S3 Storage Lab

This lab demonstrates the creation and management of Amazon S3 storage, including uploading objects, managing permissions, testing connectivity from EC2, applying bucket policies, and exploring versioning.

---

## **Task 1: Create a Bucket**

### **Objective**
Create a new S3 bucket to store data and learn basic configuration options such as region selection, bucket naming, and permissions.

### **Steps**
1. Log in to your AWS Management Console.
2. Navigate to **S3** service.
3. Click **Create bucket**.
4. Enter a unique **Bucket name** (e.g., `my-lab-storage-bucket`).
5. Choose your preferred **AWS Region** (same region as your EC2 instance for cost efficiency and faster access).
6. Leave other settings as default for now.
7. Click **Create bucket**.

### **Key Learning**
You learned that:
- Bucket names must be globally unique across AWS.
- Region choice affects latency and data compliance.
- Default settings provide private access by default (secure configuration).

### **Screenshot**
Add your screenshot file under:  
`screenshots/task1-bucket-creation.png`

---

## **Task 2: Upload an Object to the Bucket**

### **Objective**
Upload a sample file to your S3 bucket to understand object storage and metadata.

### **Steps**
1. Open your created bucket.
2. Click **Upload** → **Add files**.
3. Select a file from your local computer (e.g., `sample.txt`).
4. Click **Upload**.

### **Key Learning**
You learned that:
- S3 objects can include files of any type.
- Each object can have metadata and unique permissions.
- Uploading doesn’t automatically make objects public.

### **Screenshot**
Add your screenshot file under:  
`screenshots/task2-upload-object.png`

---

## **Task 3: Make an Object Public**

### **Objective**
Understand S3 object-level permissions and how to make files accessible publicly.

### **Steps**
1. In your bucket, go to the **Objects** tab.
2. Select the uploaded file (e.g., `sample.txt`).
3. Go to the **Permissions** tab.
4. Under **Object Ownership**, ensure ACLs are enabled if required.
5. Scroll down to **Access Control List (ACL)** → **Edit**.
6. Grant **Public read access** to everyone.
7. Save changes.
8. Copy the **Object URL** and test it in a browser.

### **Key Learning**
You learned that:
- S3 uses ACLs and bucket policies for access management.
- Making objects public exposes them via a direct HTTP endpoint.
- Public read should only be used for controlled cases (e.g., static websites).

### **Screenshot**
Add your screenshot file under:  
`screenshots/task3-make-object-public.png`

---

## **Task 4: Test Connectivity from EC2 Instance**

### **Objective**
Verify that your EC2 instance can access your S3 bucket, testing AWS network communication and permissions.

### **Steps**
1. Go to your EC2 instance and connect using **EC2 Instance Connect** or **SSH**.
2. Run the following command in the terminal:

   ```bash
   aws s3 ls s3://my-lab-storage-bucket
3. You should see a list of the uploaded files

### **Key Learning**
- EC2 instances require an IAM role with S3 permissions to access buckets securely.
- The AWS CLI is used to interact with S3 without a web browser.
- Proper IAM configuration eliminates the need for embedding AWS keys in code.

### **Screenshot**
Add your screenshot file under:  
`screenshots/task4-test-connectivity.png`

---

## **Task 5: Create a Bucket Policy**

### **Objective**
Apply a bucket policy to control access permissions for all objects within your bucket.

### **Steps**
1. Open your S3 bucket.
2. Go to the **Permissions** tab.
3. Scroll down to **Bucket Policy** → **Edit**.
4. Paste the example policy below, replacing my-lab-storage-bucket with your actual bucket name:
5. Save changes.
6. Test the policy by opening your object's public URL again.

### **Key Learning**
- Bucket policies apply to all objects in the bucket.
- The "Principal": "*" grants public access to anyone.
- JSON structure defines AWS permissions: "Effect", "Action", and "Resource".
- It’s best practice to test policies with specific IAM roles before applying public access.

### **Screenshot**
Add your screenshot file under:  
`screenshots/task5-create-bucket-policy.png`

---

## **Task 6: Exploring Versioning**

### **Objective**
Enable and test versioning to track and recover previous versions of S3 objects.

### **Steps**
1. Open your S3 bucket.
2. Go to the Properties tab.
3. Scroll to Bucket Versioning → Click Edit.
4. Enable Versioning and click Save changes.
5. Upload the same file (e.g., sample.txt) again with modified content.
6. Open your bucket and verify multiple versions are listed for the same object.

### **Key Learning**
- Versioning preserves older object versions automatically.
- It allows rollback and recovery from accidental overwrites or deletions.
- Additional storage cost applies for each version.
- Combining versioning with Lifecycle rules helps manage storage efficiently.

### **Screenshot**
Add your screenshot file under:  
`screenshots/task6-exploring-versioning.png`