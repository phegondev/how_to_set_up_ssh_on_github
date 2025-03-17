# Set Up SSH on GitHub (Mac & Windows)

Follow these step-by-step instructions to configure SSH keys for GitHub on **Mac** and **Windows**.

## 🚀 Steps to Set Up SSH on GitHub

### 1️⃣ Check Git Version  
Run the following command to verify that Git is installed:  
```sh
git --version
```

- **For Mac:** Install Xcode Command Line Tools  
  ```sh
  xcode-select --install
  ```
- **For Windows:** Download Git Bash 👉 [Download Git for Windows](https://git-scm.com/downloads/win)

---

### 2️⃣ Check if SSH Key Already Exists  
- **Mac/Linux:**  
  ```sh
  ls -al ~/.ssh
  ```
- **Windows (Git Bash):**  
  ```sh
  ls ~/.ssh
  ```

---

### 3️⃣ Generate a New SSH Key  
Run the following command, replacing `youremail@example.com` with your email:  
```sh
ssh-keygen -t ed25519 -C "youremailhere@example.com"
```

---

### 4️⃣ Save the SSH Key  
Press **Enter** to accept the default location:  


---

### 5️⃣ Add a Passphrase (Optional)  
- Press **Enter** to skip  
- Or enter a passphrase for additional security  

---

### 6️⃣ Start the SSH Agent  
- **Mac/Linux:**  
  ```sh
  eval "$(ssh-agent -s)"
  ```
- **Windows (PowerShell):**  
  ```sh
  Start-Service ssh-agent
  ```

---

### 7️⃣ Add SSH Key to SSH Agent  
```sh
ssh-add ~/.ssh/id_ed25519
```

---

### 8️⃣ Copy Your Public Key  
```sh
cat ~/.ssh/id_ed25519.pub
```

---

### 9️⃣ Add SSH Key to GitHub  
1. Go to **GitHub Settings**  
2. Navigate to **SSH & GPG Keys**  
3. Click **Add SSH Key**  
4. Paste your copied public key  

---

### 🔟 Clone Your Repository Using SSH  
Test if everything is set up correctly by cloning a repo:  
```sh
git clone git@github.com:USERNAME/REPOSITORY.git
```

---

✅ **Done!** You can now securely push and pull code using SSH. 🚀  

---

### 💡 Need Help?  
If you run into any issues, check out GitHub’s official documentation:  
👉 [GitHub SSH Key Setup](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)  

---
