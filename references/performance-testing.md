# Performance Testing — QA Engineering

## Page Load Performance (Top 5 pages)
- Record: total requests, transfer size, LCP, FCP, TTFB
- Flag any page >3s LCP
- Flag any page >50 requests on load
- Flag any single request >2s

## N+1 Query Detection
- On list pages with 10+ records: check Network tab
- Verify NOT making 1 request per row
- Expected: 1-3 requests for list data

## Bundle Analysis
- Flag chunks >500KB
- Verify code splitting per route
- Verify lazy loading for heavy components
- Check for tree-shaking (no dead code in bundle)

## Image Optimization
- Flag images >500KB
- Verify next/image or equivalent (lazy load, proper sizing)
- Check for WebP/AVIF formats
- Verify no uncompressed images served

## Memory Leak Detection
- Navigate 10+ pages rapidly — no memory increase
- Open/close 10 modals — no degradation
- Switch views 10 times — remains responsive

## Network Conditions
- Test key flows on simulated slow connection
- Verify graceful degradation
- Check for timeout handling

## Data Volume
- Test lists with 0, 1, 10, 100, 1000+ records
- Verify pagination, virtualization
- Check UI doesn't break with empty or large datasets

## API Response Times
- Baseline response times for key endpoints
- Flag any >500ms for simple queries
- Flag any >2s for complex queries
