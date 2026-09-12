# Security+ SYO-701 Hash-Integrity

## Objective
Demonstrate data integrity using SHA-256 hashing algorithm to verify file authenticity

## Lab steps
1. #### Create a demo.txt
```bash
   echo "This is demo file for hash integrity" > demo.txt
   ```
2. #### Generate hash of demo.txt
```bash
   sha256sum demo.txt > hashed_demo.txt
```
3. #### Modifying demo.txt to compromise integrity
```bash
   echo "This file has been modified" > demo.txt
```
4. #### Again generate hash of demo.txt
```bash
   sha256sum demo.txt > modified_demo.txt
```
5. #### Compare both hashes
```bash
   diff hashed_demo.txt modified_demo.txt
```
#### Expected Results
- The hashes will be different, demonstrating that even small changes to data will produce completely different hashes.
- This proves the integrity of the original data has been compromised.
## My Lab results: 

### demo.txt creation:
<img width="1278" height="798" alt="Screenshot (25)" src="https://github.com/user-attachments/assets/de5d00c6-0f08-4dde-bba0-3b795c451ff3" />

### Generating hash of demo.txt:
<img width="1920" height="927" alt="Screenshot (26)" src="https://github.com/user-attachments/assets/bdf68fd0-6992-4539-8d24-7545ff8e2dc3" />

### Modifying demo.txt:
<img width="1920" height="936" alt="Screenshot (27)" src="https://github.com/user-attachments/assets/7e25845d-1185-47da-b210-96a6ae1b47dc" />

### Generating hash again for that modified demo.txt:
<img width="1920" height="945" alt="Screenshot (28)" src="https://github.com/user-attachments/assets/a7bf1c7b-2d7a-4f67-bd16-9eb197b80654" />

### Comparing both hashes:
<img width="1920" height="946" alt="Screenshot (29)" src="https://github.com/user-attachments/assets/f4cc2162-defe-471c-8d0e-536476eb2ca2" />

## Key Points
- Hash functions are deterministic which means same input always produces same output.
- Even minor changes produce completely different hashes.
- Hashing is essential for data integrity verification.
- SHA-256 is a cryptographically secure hash function.
