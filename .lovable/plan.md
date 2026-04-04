

## Plan: Implement All Proposed Changes from Documents

Based on both documents (`earn_model1.docx` and `proposed_docx.docx`), here are all the changes organized by file.

---

### Summary of Changes

**Landing Page** (`Landing.tsx`):
1. Add "A DIGITAL LEARN & EARN ECO SYSTEM" tagline below the e@Akhuwat logo
2. Add social media buttons at the extreme bottom
3. Footer copyright: "© 2026 ALL RIGHTS RESERVED e@Akhuwat"
4. Add back button from dashboard to wallet connect interface (already handled by existing flow)

**Dashboard** (`Dashboard.tsx`):
1. Rename "HUB" → "EARN" everywhere
2. Rename "Details" button → "Portfolio" (highlighted)
3. Add "Courses" button (bold, highlighted) on overview home page
4. Replace "142 Nodes" → "142 Total Participants" (no more "Nodes" word)
5. Remove "Here's your" before "Dashboard Overview" — just say "Dashboard Overview"
6. Change Level 5 (Quantum Leader) color from pink `#f472b6` to a distinctly different vibrant color like electric orange `#f97316`
7. Change Level 6 (Supreme Visionary) color from rose `#fb7185` to a bold indigo/deep blue `#6366f1`
8. Add "Earning Workspace (Fiverr/Upwork style)" as a Coming Soon card below Daily Income
9. Add note at bottom of Plans tab: "In case of no joining, system auto flushes awaiting ID as per the above schedule" (already present in FlushoutScheduleCard)
10. Update DashboardData.ts: `planBadges` prices to $5/$10/$20/$40/$80/$160, `depositPlans` to 6 plans with correct prices
11. Update `scheduleNotes` to match 6 plans with correct cadence (3/8/16/25/40/60 days)
12. Profile page: show all active plans if user has multiple, replace "Level 4 Node" with "Plan 4 Active" or similar
13. Add profile name, picture, and ID on dashboard overview below "Welcome Back"
14. Hide Admin Panel from all users (menu item removed from sidebar/bottom nav)
15. Add PROMO button placeholder on dashboard
16. Move social media links from Admin Panel to a prominent place

**DashboardData.ts**:
1. Update `planBadges` to 6 plans with correct prices
2. Update `depositPlans` to 6 plans with earn model prices
3. Update `poolStats` — replace "Nodes" with "Total Participants"
4. Update `scheduleNotes` to 6 plans

**ProfilePanel.tsx**:
1. Show all active plans (not just one)
2. Replace "Node" terminology with simple words like "Active Account"

**BottomNav.tsx** / **InternalSidebar.tsx**:
1. Hide Admin Panel menu item from regular users

---

### Technical Details

**File 1: `src/components/Landing.tsx`**
- Add subtitle text "A DIGITAL LEARN & EARN ECO SYSTEM" under the logo SVG
- Update footer copyright text

**File 2: `src/components/Dashboard.tsx`**
- Rename "Details" → "Portfolio" in overview action buttons (line 835)
- Remove "Here's your" — change line 831 to just "Dashboard Overview"
- Add "Courses" button in the 3-column grid (make it 4-column or replace Refer with Courses and keep Refer in network only)
- Replace "Nodes" → "Total Participants" in PoolStatsCard (line 526)
- Change Level 5 theme: `primary: '#f97316'` (orange), `secondary: '#ea580c'`, matching glow/bgGlow/text
- Change Level 6 theme: `primary: '#6366f1'` (indigo), `secondary: '#4f46e5'`, matching glow/bgGlow/text
- Add second ComingSoonCard for "Earning Workspace" (Fiverr/Upwork style)
- Add user profile info (name, picture, ID) below "Welcome Back" heading
- Add PROMO button placeholder

**File 3: `src/components/dashboard/DashboardData.ts`**
- Update `planBadges` array to 6 plans: $5, $10, $20, $40, $80, $160
- Update `depositPlans` array to 6 plans with correct prices
- Update `poolStats`: "142 Nodes" → "142 Total Participants"
- Update `scheduleNotes` to 6 plans with correct flush-out cadence

**File 4: `src/components/ProfilePanel.tsx`**
- Replace "Node" with "Active Account"
- Show multiple active plans if enrolled in more than one

**File 5: `src/components/BottomNav.tsx`**
- Remove or hide Admin Panel from navigation

**File 6: `src/components/EdTechSpace.tsx`**
- Update Level 5 and 6 color themes to match new colors

