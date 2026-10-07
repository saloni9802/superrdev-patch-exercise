# Patch Notes

## Changes Made

1. Fixed task search filtering in `TaskRepository.java` by grouping the title/description search conditions correctly with the archived and status filters.
2. Removed an artificial `Thread.sleep()` delay from `TaskController.java` that unnecessarily slowed search requests.
3. Fixed the frontend loading state in `useTasks.js` so loading stops when an API request fails, and stale errors are cleared before a new request.

## What I Did Not Change

I did not modify the task entity, status enum, API request format, or UI components because they worked as expected during testing.

## Biggest Remaining Risk

The application uses an in-memory H2 database, so task data is not persistent across application restarts.

## Tools / AI Used

Used VS Code for code changes and testing. Used ChatGPT to help inspect the code, identify likely issues, understand root causes, and verify focused fixes.