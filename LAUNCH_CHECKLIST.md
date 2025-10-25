# Sturgeon AI - Launch Checklist

Estimated Time: 30 minutes
For Production Deployment: https://sturgeon-ai-prod.vercel.app

## 😈 CRITICAL Items (MUST DO)

 - [ ] GitHub Secrets - Add to ALL 4 repos
    - [ ] DATABASE_URL (Supabase Postgres Connection)
    - [ ] SUPABASE_ANON_KEY (From Supabase Dashboard)
    - [ ] SUPABASE_SERVICE_KEY (From Supabase Dashboard)
    - [ ] OPENAI_API_KEY (From OpenAI Console)
    - [ ] SECREV_KEY (Generate random 32 chars)
    - [ ] SENTRY_DSN (Create Sentry account)

 - [ ] Supabase Configuration
    - [ ] Enable RLS Policies on all tables
    - [ ] Whitelist Vercel IPs in Firewall
    - [ ] Test Database Connection with curl test

 - [ ] FastAPI Code Updates
    - [ ] Update from enhanced-main.py
    - [ ] Add JWT Authentication Middleware
    - [ ] Add Rate Limiting (SlowAPI 9.1.9)
    - [ ] Add Global Error Handlers
    - [ ] Add JSON Full Logging
    - [ ] Add OpenAPI/Swagger Config
    - [ ] Update requirements.txt

 - [ ] Test Deployment
    - [ ] `curl https://sturgeon-ai-prod.vercel.app/health` (Expected: 200)
    - [ ] `curl https://sturgeon-ai-prod.vercel.app/api/docs` (Swagger Enabled)
    - [ ] `curl https://sturgeon-ai-prod.vercel.app/api/v1/organizations` (API Working)
    - [ ] Verify No Errors in Sentry Dashboard

 - [ ] OAuth2 Setup
    - [ ] Register Google OAuth
    - [ ] Register GitHub OAuth
    - [ ] Add Callback URLs (https://sturgeon-ai-prod.vercel.app/auth/callback/*)
    - [ ] Store CLIENT_IDs and CLIENT_SECRETs

 - [ ] Monitoring Setup
    - [ ] Create Sentry account at https://sentry.io
    - [ ] Get SENTRY_DSN URL
    - [ ] Add To GitHub Secrets
    - [ ] Verify Errors Appear in Sentry

## ☯ Completion Checklist
"Fire: When ALL Checkboxes Are Checked - LAUNCH READY!