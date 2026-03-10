# File Upload & Download Testing — QA Engineering

## Upload
- [ ] Valid file types accepted
- [ ] Invalid types rejected with message
- [ ] Oversized file rejected with limit message
- [ ] Special chars in filename handled
- [ ] Multiple file upload works
- [ ] Drag-and-drop works
- [ ] Progress indicator shows
- [ ] Server-side type validation (not just extension)
- [ ] Image thumbnails generated

## Download
- [ ] Download works, file matches uploaded
- [ ] Correct MIME type
- [ ] Signed URL expiration works
- [ ] Unauthorized users blocked

## Storage
- [ ] Quota enforced per tier
- [ ] Deletion frees quota
- [ ] Files cleaned on parent record delete