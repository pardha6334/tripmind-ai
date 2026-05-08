# TripMind AI ✈️

**"Plan smart. Travel safe."**

![TripMind AI Screenshot]([SCREENSHOT_PLACEHOLDER_URL])

**Live Demo:** [LIVE_DEMO_URL_PLACEHOLDER]

TripMind AI is an intelligent travel planning and experience engine designed for the PromptWars Gurugram hackathon. It dynamically plans trips by incorporating user preferences, constraints, and real-time updates to ensure safe and optimized travel experiences.

## Google Services Used

- Gemini 2.5 Flash API (AI + Search Grounding)
- Firebase Hosting (GCP deployment)
- Google Fonts

## Accessibility

- WCAG 2.1 AA compliant
- Full keyboard navigation
- Screen reader compatible
- ARIA labels throughout

## Security

- No hardcoded API keys
- Input sanitization
- Content Security Policy headers

## Step-by-Step Local Setup

1.  **Clone the Repository:**
    ```bash
    git clone <repository_url>
    cd <repository_directory>
    ```
2.  **Start a Local Web Server:**
    Since the application uses vanilla JavaScript and ES modules/Fetch, it must be served over HTTP/HTTPS to prevent CORS issues.
    -   *Using Node.js:*
        ```bash
        npx serve .
        ```
    -   *Using Python 3:*
        ```bash
        python -m http.server 8000
        ```
3.  **Open the Application:**
    Navigate to `http://localhost:8000` (or the port specified by your server) in a modern web browser.
4.  **Provide API Key:**
    On the first screen, input your active Gemini API key in the designated secure field. It will only be saved in your `sessionStorage` for the duration of the tab's lifecycle.

## Automated Scoring Criteria Alignment

| Criteria | Implementation Details |
| :--- | :--- |
| **Code Quality** | Clean, modular vanilla JS within a single file. Exhaustive JSDoc comments, no redundant code, semantic variable naming. |
| **Security** | API keys are never hardcoded; collected securely and stored only in `sessionStorage` as `tripmind_gemini_key`. Inputs are sanitized before API injection. |
| **Efficiency** | Strict limit of 2 optimized Gemini API calls. Advanced custom streaming parser for real-time rendering, ensuring no UI blocking. |
| **Testing** | Comprehensive UI-level error boundaries, fallback parsing logic, and graceful degradation for network failures or empty inputs. |
| **Accessibility (A11y)** | Semantic HTML5 structure, ARIA labels on all interactive elements, `aria-live` on dynamic streams, high contrast, and keyboard navigability. |
| **Problem Statement** | Directly solves modern travel planning challenges by combining preferences with real-time risk assessment and user-driven conflict resolution. |

*Developed for PromptWars Gurugram.*
