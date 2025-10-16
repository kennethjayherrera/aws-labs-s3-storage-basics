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