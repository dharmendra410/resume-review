# Resume Review

A standalone browser-based resume review web page. It compares a resume against a job description, shows a match score, highlights matched and missing keywords, suggests improvements, generates key points, creates a 90% match resume draft, and lets users download the review as a PDF.

## Features

- Paste a job description and resume text
- Upload PDF files for job description or resume
- Generate a resume match score
- View matched and missing keywords
- Get suggested resume improvements
- Get key points to add
- Generate a 90% match resume draft
- Copy or download the resume draft as TXT
- Download the full review result as PDF
- Add user reviews on the page
- Responsive royal-blue themed design

## Project Files

- `index.html` - main deploy-ready page for Vercel or any static host
- `outputs/resume-review.html` - original standalone page
- `outputs/index.html` - copy of the main page for output-folder deployment
- `outputs/resume-review-project.zip` - packaged project files

## How To Run Locally

Open `index.html` directly in a browser.

You can also open:

```text
outputs/resume-review.html
```

No build step is required because this is a single HTML, CSS, and JavaScript project.

## PDF Upload Note

PDF text extraction uses PDF.js from a CDN:



So PDF upload needs internet access. Manual paste, scoring, suggestions, resume draft, user reviews, and PDF result download work from the local page.

## How To Deploy On Vercel

Deploy the project root folder:

```text
C:\Users\dharmendra jat\Documents\2026-06-21\mma
```

Vercel should serve `index.html` at the homepage route `/`.

If you deploy only the `outputs` folder, make sure Vercel uses:

```text
outputs/index.html
```

## Common Vercel NOT_FOUND Fix

If Vercel shows `NOT_FOUND`, it usually means the deployed folder does not contain an entry page for `/`.

For this project, the fix is to make sure `index.html` exists in the folder you deploy. This project includes:

```text
index.html
outputs/index.html
```

## Usage

1. Paste the job description.
2. Paste or upload the resume.
3. Click `Review Resume`.
4. Read the score, keywords, suggestions, and key points.
5. Copy or download the generated resume draft.
6. Click `Download Review PDF` to save the full result.

## Tech Stack

- HTML
- CSS
- Vanilla JavaScript
- PDF.js for reading uploaded PDF text
- Built-in browser Blob download for generated TXT and PDF files

## Privacy

The review logic runs in the browser. Text pasted into the page is processed locally by the page script. PDF.js is loaded from a CDN for PDF extraction.
