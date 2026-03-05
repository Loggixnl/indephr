# IndepHR SendGrid Email Templates

## Templates

### 1. Survey Invitation (`survey-invitation.html` / `.txt`)

Used to invite employees to participate in a feedback survey. Emphasizes anonymity and the value of their input.

## Template Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{first_name}}` | Recipient's first name | Sarah |
| `{{company_name}}` | Name of the organization | TechCorp Netherlands |
| `{{survey_name}}` | Title of the survey | Q1 2024 Employee Engagement Survey |
| `{{survey_url}}` | Unique link to the survey | https://survey.indephr.com/abc123 |
| `{{estimated_time}}` | How long the survey takes | 5-7 minutes |
| `{{deadline}}` | Survey closing date | Friday, March 15, 2024 |
| `{{logo_url}}` | URL to hosted company/IndepHR logo | https://... |
| `{{preheader_text}}` | Preview text (optional extension) | |
| `{{current_year}}` | For copyright notice | 2024 |
| `{{privacy_url}}` | Link to privacy policy | https://indephr.com/privacy |
| `{{unsubscribe_url}}` | SendGrid unsubscribe link | {{{unsubscribe}}} |

## SendGrid Setup

### 1. Create Dynamic Template

1. Go to SendGrid Dashboard > Email API > Dynamic Templates
2. Click "Create a Dynamic Template"
3. Name it: `IndepHR - Survey Invitation`
4. Add a version and paste the HTML content
5. Note the Template ID (e.g., `d-xxxxxxxxxxxx`)

### 2. Configure Unsubscribe

Replace `{{unsubscribe_url}}` with SendGrid's built-in tag:
```
{{{unsubscribe}}}
```

### 3. Test the Template

Use SendGrid's preview feature with test data:

```json
{
  "first_name": "Sarah",
  "company_name": "TechCorp Netherlands",
  "survey_name": "Q1 2024 Employee Engagement Survey",
  "survey_url": "https://survey.indephr.com/test123",
  "estimated_time": "5-7 minutes",
  "deadline": "Friday, March 15, 2024",
  "logo_url": "https://your-cdn.com/indephr-logo.png",
  "current_year": "2024",
  "privacy_url": "https://indephr.com/privacy"
}
```

## Brand Guidelines Applied

- **Colors**:
  - Primary Blue: `#1A4F89`
  - Orange (CTA): `#F7931E`
  - Purple: `#6F288D`
  - Grays: `#374151`, `#6B7280`, `#9CA3AF`

- **Typography**:
  - Headings: Montserrat (600, 700)
  - Body: Open Sans (400, 600)

- **Tone**: Professional, empathetic, empowering

## Future Templates

Suggested additional templates to create:

1. **Survey Reminder** - Nudge for non-respondents before deadline
2. **Survey Closing Soon** - Final reminder (24-48 hours before close)
3. **Thank You** - Confirmation after survey completion
4. **Results Available** - Notify when reports are ready
5. **Action Plan Update** - Share what actions were taken based on feedback

## Troubleshooting

### Images not displaying
- Ensure images are hosted on a publicly accessible URL
- Use HTTPS URLs only
- Add `alt` text for accessibility

### Button not clickable in Outlook
- The template uses a bulletproof button approach
- If issues persist, add VML fallback for Outlook

### Fonts not rendering
- Google Fonts may not load in all email clients
- Arial is set as fallback font
