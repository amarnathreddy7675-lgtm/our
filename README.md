# OUR UNIVERSE
Phase 1 (proposal gate, navigation, overview) plus the full database/storage schema.

    npm install && npm run dev

## Supabase setup (Phase 2 prerequisites)
1. Create a project. Auth settings: **disable public sign-ups**.
2. Create the two users in Authentication > Users.
3. Run `supabase/migrations/0001_init.sql`.
4. Insert one `relationship_settings` row and two `relationship_members` rows (SQL editor).
5. Copy `.env.example` to `.env.local` and fill it in. Never expose the service-role key.

## Status
Done: proposal gate, escaping NO + accessible decline, nav, overview counter (Asia/Kolkata), schema + RLS.
Auth removed by design (open site). Not yet built: Our Story, Memories, Love Letters, Memory Map. Nothing has been run or tested yet.
Videos (up to 50 MB each) work in Memories and Scratch & Reveal; stored in this browser.

## Put it online with shared data (Supabase)
1. Create a free project at supabase.com. Run `supabase/schema.sql` in the SQL Editor.
2. Project Settings > API: copy the Project URL and the anon public key.
3. Put them in `.env.local` (see `.env.example`) and in Vercel > Settings > Environment Variables, then redeploy.
Without these variables the site stores data in the browser only. The site is open: anyone with the link can view and edit.
"# our" 
