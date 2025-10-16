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