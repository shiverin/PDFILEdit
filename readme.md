# PDF Management Web Application

This Flask-based web application allows users to upload, manage, merge, download, and delete PDF files, along with additional features such as signature tools and zip file creation. The app is designed for users to interact with their files via a session-based approach, keeping each user's data isolated.

## Features

- **File Upload**: Users can upload multiple PDF files.
- **Merge PDFs**: Users can merge multiple PDFs into a single file with a custom name.
- **Download PDF**: After merging, users can download the merged PDF file.
- **Delete Files**: Users can delete individual files from their session.
- **Clear All**: Admins can clear all uploaded files for all users or individual users.
- **Create ZIP**: Users can zip all uploaded files and download them as a `.zip` file.
- **Signature Tool**: A page for adding signatures to PDF files.
- **Session Management**: Each user gets a unique session ID for file management.

## Setup and Installation

### Prerequisites

- Python 3.x
- Flask
- werkzeug
- Any other Python dependencies required for your project.

### Install the dependencies

You can install the required dependencies by running the following command:

```bash
pip install -r requirements.txt
