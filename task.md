# Task Checklist: Best Thirds Manual Overrides

- [x] Refactor `GroupRankEditor` data fetching and hooks to support the `"3rd"` (Mejores Terceros) group letter option
- [x] Add `"3rd"` selector option to the `GroupRankEditor` UI dropdown and format team rows with group letter badges
- [x] Modify best third-placed teams sorting logic in `resolvedTeamsMap` to respect manual overrides
- [x] Modify best third-placed teams sorting logic in `PositionsTab` to respect manual overrides
- [x] Update database save helper `handleAdminUpdateGroupOverrides` to support generic labels for groups and best thirds
- [x] Update `walkthrough.md` to document the changes

# Task Checklist: Tab State & Scroll Position Preservation
- [x] Refactor conditional tab mounting in `index.html` to CSS `hidden` class wrapper elements
- [x] Implement a `useRef` to store scroll positions of each tab in `App` component
- [x] Define a `handleTabChange` function to record scroll positions before active tab state changes
- [x] Add a `useEffect` hook to restore tab scroll positions when the active tab is changed
- [x] Verify layout and update the `walkthrough.md` documentation

# Task Checklist: Browser Tab Focus Reload Bug
- [x] Add an `isInitial` parameter to the `fetchUserData` function
- [x] Conditionally trigger `setAuthLoading(true)` only when `isInitial` is true
- [x] Update the initial auth session listener to pass `isInitial = true` to `fetchUserData`
- [x] Update the realtime `onAuthStateChange` listener to pass `isInitial = !user` (false if user is already logged in)
- [x] Document the resolution in `walkthrough.md`

