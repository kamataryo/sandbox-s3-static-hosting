# how to hosting

## create

```shell
$ aws s3 mb s3://s3-static-hosting-lesson
$ aws s3 ls
$ aws s3 website s3://s3-static-hosting-lesson \
  --index-document index.html \
  --error-document error.html
$ aws s3 sync ./public/ s3://s3-static-hosting-lesson
$ aws s3 ls s3://s3-static-hosting-lesson
# set bucket policy
$ aws s3api put-bucket-policy \
  --bucket s3-static-hosting-lesson \
  --policy file://./policy.json

$ open http://s3-static-hosting-lesson.s3-website-ap-northeast-1.amazonaws.com
```

## remove

```shell
$ aws s3 rm s3://s3-static-hosting-lesson/index.html
$ aws s3 rm s3://s3-static-hosting-lesson/error.html
$ aws s3 rb s3://s3-static-hosting-lesson
$ aws s3 ls
```
