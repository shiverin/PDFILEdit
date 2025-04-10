# PDF Master: A Flask-Based PDF Management Web Application

## Overview

**PDF Master** is a feature-rich web application that allows users to manage, manipulate, and process PDF files entirely through the browser. Designed as my final project for Harvard’s CS50x course, this Flask-based tool serves as a one-stop platform for common PDF operations, such as uploading, merging, deleting, and converting PDFs—along with a seamless interface to add digital signatures.

The project reflects a blend of software engineering, user experience design, and web security principles. It aims to simplify everyday PDF-related tasks that users would otherwise need multiple desktop tools or paid services for. With an intuitive UI and secure backend, PDF Master is built to be lightweight yet powerful—suitable for both individual users and small businesses.

---

## Key Features

- **Upload PDFs**: Users can upload PDF files which are automatically sorted into session-specific directories.
- **Delete PDFs**: Users can remove unwanted PDFs from their session folders.
- **Merge PDFs**: Select and combine multiple PDFs into a single file.
- **Download PDFs**: Easily download individual PDFs or merged outputs.
- **Session Management**: Each user is assigned a unique session ID ensuring private, isolated file access.
- **Secure File Handling**: Prevents malicious file uploads through validation.
- **Signature Support** *(in progress)*: Upload, draw, and apply digital signatures to any page of a PDF file.

---

## Why It’s Impactful

Handling PDF files is a daily necessity for students, professionals, and institutions alike. Existing solutions are often either expensive, bloated, or require installation. PDF Master brings these capabilities to the web with a lightweight and responsive experience.

This project also explores the integration of key software development principles, such as secure file management, session-based access, modular routing in Flask, and dynamic template rendering. It emphasizes real-world skills and reflects my commitment to building practical, scalable tools as I transition into software development full-time.

---

## Technologies Used

- **Flask**: A lightweight Python web framework used for handling routes, sessions, and server logic.
- **HTML/CSS**: For creating a responsive and clean front-end interface.
- **Jinja2**: Flask’s templating engine, used to dynamically render user-specific data.
- **Werkzeug**: Specifically, `secure_filename` is used to safely handle uploaded filenames.
- **uuid** and **secrets**: For generating unique session identifiers and managing secret keys.
- **PyPDF2**: A powerful Python library used to manipulate PDF files, including merging and page extraction.
- **os** and **shutil**: For creating, cleaning, and managing user-specific file directories.

---

## Challenges Faced

### 1. **File Isolation and Session Management**
One of the biggest architectural decisions involved implementing session-based file isolation. Each user session needed its own unique folder where files are uploaded and processed. Flask’s built-in session tools helped, but I also used UUIDs to reinforce session uniqueness and security.

### 2. **Post-Processing Cleanup**
Since files are stored server-side, it was important to implement cleanup mechanisms to delete session data after downloads. This ensures server space is preserved and minimizes the chance of cross-user file access.

### 3. **Secure Upload Handling**
Preventing dangerous file uploads was a key concern. Although file extensions were validated, I researched MIME type checking for future improvements using `python-magic`.

### 4. **User Feedback and Experience**
Flash messages were implemented to improve the user experience—alerting users when actions like uploads, deletions, or merges succeeded or failed.

---

## Installation Instructions

To run PDF Master locally on your machine, follow these steps:

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/pdf-master.git
cd pdf-master
