# functions ports : 
lamba: aws --endpoint-url=http://localhost:4566 

# Tips
## lambdas
aws --endpoint-url=http://localhost:4566 lambda list-functions


## logs
aws --endpoint-url=http://localhost:4566 logs describe-log-groups
aws --endpoint-url=http://localhost:4566 logs describe-log-streams \
  --log-group-name "/aws/lambda/GetBalance"

aws --endpoint-url=http://localhost:4566 logs get-log-events \
  --log-group-name "/aws/lambda/GetBalance" \
  --log-stream-name "2025/08/27/[$LATEST]xxxxxxxx" \
  --limit 20