
# Run the ml model as a server
```bash
mlflow models serve -m mlruns/0/00dfa9874f544592bb652d061765da87/artifacts/model_random_forest --no-conda
```

Then 

```bash
curl http://127.0.0.1:5000/invocations -H 'Content-Type: application/json' -d '{"inputs":[[1,1,1,1,0,1,1,1,0,1,1,1,0,0]]}'
```