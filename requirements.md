# Requirements - Authentic-AI Content Hub

## 1. Overview
Authentic-AI is a web-based hub designed to restore digital trust by verifying the provenance of digital assets.

## 2. Functional Requirements (EARS Notation)
- **[RE-01]** WHEN a user drags and drops an image or video into the UploadZone, THE SYSTEM SHALL initiate a metadata scan.
- **[RE-02]** THE SYSTEM SHALL extract C2PA and Exif metadata to identify the origin of the digital asset.
- **[RE-03]** WHEN AI-generated markers are detected, THE SYSTEM SHALL calculate a 'Synthetic Content' percentage score.
- **[RE-04]** THE SYSTEM SHALL display a 'Content Nutrition Label' that breaks down Human Input vs. AI Assistance.
- **[RE-05]** THE SYSTEM SHALL provide a 'Provenance Timeline' showing the edit history of the file.
- **[RE-06]** IF no metadata is found, THE SYSTEM SHALL display an "Unverified Source" warning to the user.

## 3. Non-Functional Requirements
- **[NFR-01]** The system UI shall be built using React and Tailwind CSS with a focus on glassmorphism.
- **[NFR-02]** Metadata analysis should complete within 3 seconds for images under 5MB.
