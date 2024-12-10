
# NOTEVAULT
NoteVault is a cloud-based note-taking platform designed to help users easily create,
organize, and access their notes in a secure and user-friendly environment. 


## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [AI Powered Tools](#ai-powered-tools)
- [Technologies used](#technologies-used)
- [Instructions to setup](#instructions-to-setup)

---

## Overview
**Note Vault** is a web application designed to help users manage and organize their notes efficiently. It offers features for creating, editing, categorizing, and sharing notes, along with AI-powered tools for content enhancement. Users can also manage their profile settings for a personalized experience.

---

## Key Features

### 1. Notes Management

- **Create, View, Edit, and Delete Notes:**
  - Users can create new notes, update existing ones, or delete them.
  - Each note has the following attributes:
    - **Title:** A title for the note content.
    - **Category:** Organize notes into customizable categories.
    - **Font Size:** Choose the font size for note content.
    - **Font Style:** Select the font style for the note content.
    - **Fix Spelling and Grammar:** Automatically correct spelling and grammar errors in the note content.
    - **Summarize with AI:** Use AI to generate a summarized version of the note.
    - **Speech-to-Text:** Convert spoken words into note content by clicking on the microphone button. *(Not deployed to EC2)*
    - **Reset:** Clear all content within a note.

---

### 2. Categories Management

- **View Categories:** Display a list of categories. Clicking on a category will show the associated notes.
- **Add Category:** Allow users to create new categories for organizing their notes.
- **Update Category:** Users can modify the title of an existing category.
- **Delete Category:** Deleting a category will remove both the category and the notes associated with it.

---

### 3. Note Interaction

- **Pin Notes:** Pin important notes to keep them at the top of the note list for easy access.
- **Search:** Search for notes by title or content.
- **Copy:** Duplicate an existing note.
- **Download:** Export a note as a Word document, preserving the original font size and style.

---

### 4. User Profile & Settings

- **View Profile:** Display user profile information, including account settings and preferences.
- **Logout:** Allows users to securely log out of their account.

---

## AI-Powered Tools

**Note Vault** leverages generative AI (GenAI) to enhance productivity and streamline note-taking:

- **Summarization:** Automatically generate concise summaries of lengthy notes, helping you quickly grasp key points.
- **Spell-Check and Grammar Fix:** Correct errors effortlessly to maintain professional-quality content.
- **Speech-to-Text:** Use voice input for hands-free note-taking, making it easy to capture ideas on the go.---

---

## Technologies Used
### Frontend:
1. React.js (with React Router for navigation)
2. TailwindCSS (for styling)
3. Framer Motion (for animations)

### Backend:
1. Django
2. Django REST Framework
3. MongoDB (via Djongo)

---

## Instructions to set up

Clone the Repository

```
git clone https://github.com/CharanKasala/NoteVault.git
cd NoteVault  
```

#### Frontend (React): 

Navigate to the Frontend Directory and Install Dependencies
```
cd frontend
npm install
```

Run the Development Server
```
npm start
```
This will run the React app at http://localhost:3000.


#### Backend (Django):

Navigate to the Backend Directory
```
cd ../notevaultBackend
```

Create a Virtual Enivronment if you need
```
python -m venv "name-of-vir-env"

Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Unrestricted

name-of-vir-env\Scripts\activate
```

Install Python Dependencies
```
pip install -r requirements.txt
```

Set Up the Environment Variables 
```
DATABASE_URL=mongodb+srv://<your_mongodb_cluster>
```

Run Database Migrations
```
python manage.py makemigrations
python manage.py migrate
```

Start the Django Development Server
```
python manage.py runserver
```

This will run the backend server at http://localhost:8000.
