Mini Version Control System (VCS)
Mini VCS is a simple, file-based version control system implemented in Python. It allows users to:
✅ Initialize a repository 🏗️

✅ Create snapshots (save the current state of files) 

✅ Revert to previous snapshots

🏗 1. Project Structure
bash
Copy
Edit
mini-vcs/
│── .vcs_storage/   # Stores snapshots
│── vcs.py   # Main VCS script
│── README.md   # Documentation
│── .gitignore   # Optional (to ignore vcs_storage)
🚀 2. Installation & Setup
🛠 Step 1: Clone the Repository
sh
Copy
Edit
git clone https://github.com/yourusername/mini-vcs.git
cd mini-vcs
🛠 Step 2: Run the VCS Commands
🔹 Initialize the VCS
sh
Copy
Edit
python vcs.py init
This creates a .vcs_storage directory to store snapshots.

🔹 Create a Snapshot
sh
Copy
Edit
python vcs.py snapshot
Saves the current state of all files (excluding .vcs_storage). A unique hash is assigned to each snapshot.

🔹 Revert to a Snapshot
sh
Copy
Edit
python vcs.py revert <snapshot_hash>
Restores all files to a previous snapshot state and removes extra files not present in the snapshot.

🛠 3. How It Works
🔹 Snapshot Creation Process
Reads all files (except .vcs_storage)
Computes a SHA-256 hash for the snapshot
Saves files in .vcs_storage/<hash>
🔹 Reverting Process
Loads the selected snapshot
Restores files to their saved state
Removes extra files that were not in the snapshot
🎯 4. Why Use This?
✅ Simple & Lightweight – No complex setups like Git.
✅ Fast Snapshots – Instant file versioning.
✅ Revert Anytime – Go back to a previous file state easily.
✅ Self-Contained – Works in a single Python script.

📜 5. License
This project is open-source and free to use and extremely easy to implement! 🚀


![Screenshot 2025-03-17 002805](https://github.com/user-attachments/assets/d2a2015c-59af-4f37-ba5d-908054d26c96)
![Screenshot 2025-03-17 002758](https://github.com/user-attachments/assets/1a1f951b-3996-4979-9f1e-67387501746a)
![Screenshot 2025-03-17 002749](https://github.com/user-attachments/assets/ecba88ef-9c2c-41ca-a776-bd2b94f13b61)
![Screenshot 2025-03-17 002917](https://github.com/user-attachments/assets/3e1fdc5f-455d-4b8a-92df-b24831ae8546)
