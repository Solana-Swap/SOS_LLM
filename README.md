# SOS_LLM

Intelligent market model based on Google Deepmind open source model training

[Gemma](https://ai.google.dev/gemma) is a family of open-weights Large Language
Model (LLM) by [Google DeepMind](https://deepmind.google/), based on Gemini
research and technology.

## Quick start

### Installation

1. To install Gemma you need to use Python 3.12 or higher.

2. Install JAX for CPU, GPU or TPU. Follow instructions at
    [the JAX website](https://jax.readthedocs.io/en/latest/installation.html).

3. Run

```shell
python -m venv gemma-demo
. gemma-demo/bin/activate
pip install .
```

### The models

```
7b/              # Directory containing model weights
tokenizer.model  # Tokenizer
```

*The model checkpoints is in training mode and is not available for download.*

### Running the unit tests

To run the unit tests, install the optional `[test]` dependencies (e.g. using
`pip install -e .[test]` from the root of the source tree), then:

```
pytest .
```

Note that the tests in `test.py` are skipped by default since no
tokenizer is distributed with the Gemma sources. To run these tests, download a
tokenizer following the instructions above, and update the `_VOCAB` constant in
`test.py` with the path to `tokenizer.model`.

## System Requirements

Gemma can run on a CPU, GPU and TPU. For GPU, we recommend a 8GB+ RAM on GPU for
the 2B checkpoint and 24GB+ RAM on GPU for the 7B checkpoint.

## License

Copyright 2024 SOS_LLM Authors

This code is licensed under the Apache License, Version 2.0 (the \"License\");
you may not use this file except in compliance with the License. You may obtain
a copy of the License at <http://www.apache.org/licenses/LICENSE-2.0>.

Unless required by applicable law or agreed to in writing, software distributed
under the License is distributed on an AS IS BASIS, WITHOUT WARRANTIES OR
CONDITIONS OF ANY KIND, either express or implied. See the License for the
specific language governing permissions and limitations under the License.
