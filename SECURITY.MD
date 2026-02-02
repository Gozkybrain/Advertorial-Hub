# Super Post Ads Page

## Overview

The **Super Post Ads Page** allows users to select a post and automatically generate a tailored ad strategy using AI. This feature is **experimental** and intended for users who understand social media advertising.  

**Key features:**

- AI-powered ad strategy generation
- Searchable post dropdown with typeahead suggestions
- Single-block ad display with Markdown formatting
- Copy-to-clipboard functionality for easy reuse
- Visual loading indicator while AI generates content

---

## How It Works

### Frontend

- Built with **Next.js (App Router)** and React.
- Uses a **search input** that suggests posts as the user types (minimum 4 characters).  
- AI-generated ad content is displayed in a single, clean block (`<div class="ad-text">`) with **Markdown bold support**.
- Single **“Copy All”** button copies the entire ad content, with an inline **“Copied!”** message.

### Backend / API

- The `/api/generate-ad` endpoint calls **OpenRouter AI API** using the `openrouter/auto` model.  
- Sends the selected post content and receives a structured ad strategy including:
  - Target age range
  - Gender
  - Location
  - Best platforms
  - Recommended ad budget & duration
  - Optional ad optimization tactics

### AI Prompt Engineering

- The prompt instructs the AI to:
  - Generate a complete, actionable ad strategy
  - Suggest **friendly, realistic budgets** (e.g., 3k, 5k, 10k Naira)
  - Recommend **ad duration and best times to run ads**
  - Include practical tactics like pausing ads at low-performing times
  - Keep output readable and structured

---

## UI / UX Features

- **Typeahead Search:** Only starts suggesting posts after 4 characters are entered
- **Dropdown Suggestions:** Styled dropdown under the input with hover highlighting
- **Loading Spinner:** Displays “Generating ad details…” with a rotating color rim while waiting for AI
- **Markdown Rendering:** Converts `**bold**` text into `<strong>` HTML for emphasis
- **Copy Button:** Single button for the entire ad content with inline “Copied!” feedback
- **Clean Layout:** Single-block ad content for better readability, without per-line separation

---

## Styling / CSS

- Modern, clean design using **soft backgrounds, rounded borders, and subtle shadows**
- Autocomplete dropdown and spinner animations styled for smooth UX
- Single ad block (`.ad-text`) has **white-space preserved** (`pre-line`) and proper line-height

---

## Experimental Note

> ⚠️ This feature is currently in **experimental phase**. AI-generated ad strategies should only be used by users who understand social media marketing. Results may vary, and you should verify all recommendations before running ads.

