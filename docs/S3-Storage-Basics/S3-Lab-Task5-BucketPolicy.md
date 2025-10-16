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