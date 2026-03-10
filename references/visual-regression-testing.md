# Visual Regression Testing — QA Engineering (Playwright)

## Baseline Capture
- [ ] Screenshot all critical pages at desktop, tablet, mobile
- [ ] Store baselines in version control
- [ ] Mask dynamic content (timestamps, avatars, random data)

## Comparison
- [ ] Run after code changes
- [ ] Diff threshold configured (0.1% recommended)
- [ ] Generate visual diff report
- [ ] Unexpected changes fail the test

## Browsers
- [ ] Chromium screenshots
- [ ] Firefox screenshots
- [ ] WebKit screenshots

## CI Integration
- [ ] Visual tests in CI pipeline
- [ ] Build fails on unexpected changes
- [ ] Baselines updated intentionally only