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