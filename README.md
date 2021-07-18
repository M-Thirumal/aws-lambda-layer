# aws-lambda-layer
AWS Lambda Layer tutorial
1. Create `folder` with name `python`
2. Create `python file and fucntions`
3. Create zip 
    `zip -r python.zip ./python`
   
4. Go to `AWS Lambda Layer` -> `Create layer` -> upload the `python.zip` -> choose correct runtime -> hit `CREATE` button.
5. Go to `Function` and select the uploaded layer

```
import json
import layer as la

def lambda_handler(event, context):
    # TODO implement
    print(la.layer_fun())
    return {
        'statusCode': 200,
        'body': json.dumps('Hello from Lambda!')
    }
```

### OUTPUT

```buildoutcfg
START RequestId: e2fad4b5-451f-415c-bbde-4a6127d0c231 Version: $LATEST
Hi, I am from layer_fun(), if you see me then your code is working!!!
END RequestId: e2fad4b5-451f-415c-bbde-4a6127d0c231

```