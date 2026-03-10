# Data Volume & Pagination Testing — QA Engineering

## Zero Records
- [ ] Empty state renders (not blank)
- [ ] CTA button present and works

## Single Record
- [ ] Displays correctly
- [ ] No awkward pagination ('1 of 1')

## Moderate (10-100)
- [ ] Pagination works
- [ ] Page size options work
- [ ] Column sort works
- [ ] Filter combinations work
- [ ] Search returns relevant results

## Large (1000+)
- [ ] Page loads within 3 seconds
- [ ] Pagination handles large counts
- [ ] Infinite scroll doesn't crash (if used)
- [ ] Export handles large datasets
- [ ] Search remains performant

## Extreme (10K+)
- [ ] Query doesn't timeout
- [ ] UI remains responsive
- [ ] Bulk operations don't crash