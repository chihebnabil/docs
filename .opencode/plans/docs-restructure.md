# Next-Lovable Documentation Restructure Plan

## Overview
Jobs-to-be-Done restructuring of Next-Lovable docs to support three products:
1. CLI (1 credit) - Frontend escape
2. Cloud Migration (3 credits) - Backend escape  
3. Prerendering - Production polish/SEO recovery

## Support Policy (NO FREE SUPPORT)
- **CLI/Dev Tools**: GitHub issues only for bugs
- **Cloud Migration**: Self-contained docs, paid consultation for scoping
- **Chrome Extension**: hi@remoteskills.io (bugs only)
- **Community**: Discord for peer-to-peer (no response promises)

## Structure Created

### Root
- [x] `index.mdx` - Choose Your Migration (decision tree landing)
- [x] `docs.json` - Updated navigation with anchors and tabs

### CLI Section (`/cli/`)
**Status**: 7 files created

**Files to Implement**:
- [x] `index.mdx` - CLI overview and value prop
- [x] `installation.mdx` - Install instructions (copied from 0.0.7)
- [x] `quick-start.mdx` - First conversion walkthrough (copied from 0.0.7)
- [x] `convert.mdx` - Convert command reference (copied from 0.0.7)
- [x] `migrate.mdx` - Migrate command reference (copied from 0.0.7)
- [x] `what-gets-converted.mdx` - Detailed conversion patterns
- [x] `what-breaks.mdx` - Manual fix requirements
- [x] `troubleshooting.mdx` - Common issues (copied from 0.0.7)

**Remove**: All "Contact us" references → Replace with GitHub issues link

### Cloud Migration Section (`/cloud-migration/`)
**Status**: 7 files needed

**Files to Implement**:
- [ ] `index.mdx` - Overview, escape hatch narrative
- [ ] `what-included.mdx` - Complete breakdown of migration scope
- [ ] `why-3-credits.mdx` - Polish client story, value justification
- [ ] `supabase-setup.mdx` - Preparing new Supabase project
- [ ] `migration-process.mdx` - Step-by-step process walkthrough
- [ ] `rls-policies.mdx` - Row Level Security migration
- [ ] `storage-buckets.mdx` - File and storage migration
- [ ] `auth-migration.mdx` - User accounts and password reset strategy

**Remove**: All "support@nextlovable.com" → Replace with paid consultation CTA

### Prerendering Section (`/prerendering/`)
**Status**: 5 files needed

**Files to Implement**:
- [ ] `index.mdx` - SEO recovery narrative
- [ ] `seo-recovery.mdx` - SPA vs prerendered SEO explanation
- [ ] `setup-guide.mdx` - Implementation steps
- [ ] `configuration.mdx` - Dynamic routes, caching
- [ ] `verification.mdx` - Testing Google indexing

### Pricing Section (`/pricing/`)
**Status**: 3 files needed

**Files to Implement**:
- [ ] `index.mdx` - Pricing overview
- [ ] `credit-system.mdx` - How credits work across products
- [ ] `upgrade-paths.mdx` - CLI → Cloud → Prerender → DFY

### Legacy Archive (`/legacy/0.0.6/`)
**Status**: Move existing 0.0.6 files here

**Files to Move**:
- [ ] `index.mdx`
- [ ] `installation.mdx`
- [ ] `quick-start.mdx`
- [ ] `commands/migrate.mdx`
- [ ] `guides/troubleshooting.mdx`

### Chrome Extension Docs (Future)
**Location**: TBD (separate product, consumer-focused)
**Support**: hi@remoteskills.io (bugs only)

## Content Changes Required

### Remove "Contact Us" References

**In CLI docs**:
- ❌ `support@nextlovable.com`
- ❌ "Contact us for help"
- ✅ "Found a bug? [Open a GitHub issue](https://github.com/chihebnabil/next-lovable/issues)"

**In Cloud Migration docs**:
- ❌ `support@nextlovable.com`
- ❌ "Contact us with questions"
- ✅ "Complex migrations require scoping. [Book a paid consultation](https://cal.com/nextlovable)"

**In all docs**:
- ❌ "Need help? Contact us"
- ✅ Self-serve troubleshooting
- ✅ Community Discord (peer-to-peer only)

### Update docs.json Navigation

```json
{
  "anchors": [
    {"name": "CLI", "icon": "terminal", "url": "cli"},
    {"name": "Cloud Migration", "icon": "cloud", "url": "cloud-migration"},
    {"name": "Prerendering", "icon": "bolt", "url": "prerendering"},
    {"name": "Pricing", "icon": "credit-card", "url": "pricing"}
  ],
  "navigation": {
    "tabs": [
      {
        "tab": "Documentation",
        "groups": [
          {"group": "Choose Your Migration", "pages": ["index"]},
          {"group": "Quick Start", "pages": ["cli/*"]},
          {"group": "Full Backend Migration", "pages": ["cloud-migration/*"]},
          {"group": "Production Optimization", "pages": ["prerendering/*"]},
          {"group": "Pricing & Credits", "pages": ["pricing/*"]}
        ]
      },
      {
        "tab": "Legacy Versions",
        "groups": [
          {"group": "Version 0.0.6", "pages": ["legacy/0.0.6/*"]}
        ]
      }
    ]
  }
}
```

## Implementation Order

1. ✅ Create directory structure
2. ✅ Update docs.json
3. ✅ Create root index.mdx (decision tree)
4. ✅ Copy existing CLI docs to /cli/
5. ✅ Create new CLI docs (what-gets-converted, what-breaks)
6. ⏳ Create Cloud Migration docs (8 files)
7. ⏳ Create Prerendering docs (5 files)
8. ⏳ Create Pricing docs (3 files)
9. ⏳ Move 0.0.6 to legacy/
10. ⏳ Review all docs for "contact us" references
11. ⏳ Final review and testing

## Key Messaging Points

### CLI (The Gateway Drug)
- "Stop waiting for Lovable to export"
- €79/1 credit for immediate control
- Buy the tool, not the service
- What converts vs what breaks

### Cloud Migration (The Escape Hatch)
- Infrastructure independence
- 3 credits = insurance + expertise
- Polish client story (370 tables)
- Password reset caveat

### Prerendering (Production Polish)
- "SPAs are invisible to Google"
- SEO recovery post-migration
- Included in 3-credit tier
- Standalone for existing Next.js apps

### Credit Clarity
- CLI alone: 1 credit
- Cloud Migration: 3 credits (includes CLI)
- Prerendering: Bundled or separate
- DFY: $850+ (all three handled)

## Next Steps

1. Exit Plan Mode
2. Implement remaining Cloud Migration docs
3. Implement Prerendering docs
4. Implement Pricing docs
5. Archive legacy version
6. Final review
