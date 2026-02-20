## Importing a model from Safetensors weights

[🔗 FROM](https://github.com/ollama/ollama/blob/main/docs/import.md#Importing-a-model-from-Safetensors-weights)


First, create a `Modelfile` with a `FROM` command which points to the directory containing your Safetensors weights:

```textfile
# Point to the directory containing the weights
FROM ./safetensors
```

If you create the Modelfile in the same directory as the weights, you can use the command `FROM .`.

Now run the `ollama create` command from the directory where you created the `Modelfile`:

```bash
# ollama create my-model
ollama create uncesored
```

Lastly, test the model:

```bash
# ollama run my-model
ollama run uncensored
```

Ollama supports importing models for several different architectures including:

-   Llama (including Llama 2, Llama 3, Llama 3.1, and Llama 3.2);
-   Mistral (including Mistral 1, Mistral 2, and Mixtral);
-   Gemma (including Gemma 1 and Gemma 2); and
-   Phi3

This includes importing foundation models as well as any fine tuned models which have been _fused_ with a foundation model.