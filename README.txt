
 * S3 Endpoint: http://bn.dodgson.org.s3-website-us-east-1.amazonaws.com/


----
Build:
```
$ rvm install 2.6
$ rvm use 2.6
$ nvm install --lts
$ nvm use --lts
$ bundle install
$ middleman build
```

Push:
```
$ pip3 install awscli --upgrade --user
$ ~/.local/bin/aws configure
$ ~/.local/bin/aws s3 sync --acl=public-read --delete --storage-class=REDUCED_REDUNDANCY build/ s3://bn.dodgson.org
```
