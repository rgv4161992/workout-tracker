# Workout Tracker

A recovery-driven workout tracking app with Oura Ring integration, analytics dashboard, and personal records tracking.

## Features

### Recovery System
- **Daily Check-In**: Track Oura Readiness + subjective soreness score
- **Recovery Score**: Automated calculation (Oura × 0.6 + Soreness × 0.4)
- **Color-Coded Status**: GREEN (ready), YELLOW (reduce volume), RED (rest)
- **Training Recommendations**: Personalized guidance based on recovery state

### Workout Tracking
- Log sets with exercise, reps, and weight
- Automatic set numbering per exercise
- Exercise autocomplete
- Delete individual sets
- Workout history by date

### Analytics Dashboard
- **Recovery Analytics**
  - Current recovery score
  - 7-day and 30-day averages
  - Recovery trend chart (last 30 days)
  - Check-in streak tracker
  
- **Training Analytics**
  - Weekly volume tracking
  - Volume trend chart (last 8 weeks)
  - Personal records by exercise
  - Workout frequency
  - Total sets per week

## Tech Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Charts**: Chart.js
- **Database**: PostgreSQL (via Supabase)
- **Authentication**: Supabase Auth
- **Hosting**: Vercel

## Live Demo

[https://workout-tracker-two-nu.vercel.app](https://workout-tracker-two-nu.vercel.app)

## Why This App?

Traditional workout trackers focus on progressive overload without considering recovery. This app solves the problem of overtraining by:

1. Requiring daily recovery assessment before training
2. Providing objective guidance on training intensity
3. Tracking volume to prevent excessive week-over-week increases
4. Showing recovery patterns to optimize training schedule

## Usage

### Daily Workflow
1. Open app
2. Complete daily check-in (Oura readiness + soreness)
3. View recovery status and recommendations
4. Log workout sets as you complete them
5. Check analytics to track progress

### Recovery Zones
- **80-100 (GREEN)**: Fully recovered, train normally
- **60-79 (YELLOW)**: Partial recovery, reduce volume 20-30%
- **0-59 (RED)**: Not recovered, rest or light activity only

## Database Schema

### Tables
- `users` - Authentication (managed by Supabase)
- `daily_checkins` - Recovery scores and check-in data
- `workout_sessions` - Training sessions by date
- `exercises` - Exercise library
- `sets` - Individual set data (reps, weight, exercise)

## Development

Built in a single session as a learning project.

### Local Development
1. Clone repo
2. Open `index.html` in browser
3. Update Supabase credentials in script section

## Future Enhancements

Potential features based on usage:
- Workout templates
- Rest timer
- Plate calculator
- Mobile app (React Native)
- Push notifications for daily check-in
- Export to CSV
- Integration with other fitness APIs

## License

MIT

## Author

Built to solve the personal problem of consistency through recovery-driven training.
