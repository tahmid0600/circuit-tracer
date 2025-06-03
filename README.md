# Circuit Tracer ⚡️

![Circuit Tracer](https://img.shields.io/badge/version-1.0.0-blue.svg) ![GitHub](https://img.shields.io/badge/release-v1.0.0-green.svg) ![License](https://img.shields.io/badge/license-MIT-yellow.svg)

## Overview

Welcome to the **Circuit Tracer** library! This toolset helps researchers and developers explore circuits using MLP transcoders. It builds on the foundational work of [Ameisen et al. (2025)](https://transformer-circuits.pub/2025/attribution-graphs/methods.html) and [Lindsey et al. (2025)](https://transformer-circuits.pub/2025/attribution-graphs/biology.html).

The library is designed to accomplish three key tasks:

1. **Circuit Discovery**: Identify the circuit or attribution graph in a model with pre-trained transcoders. This process calculates the direct effects of each non-zero transcoder feature, transcoder error node, and input token on each other non-zero transcoder feature and output logit.

2. **Graph Visualization**: Visualize the attribution graph and provide options for annotating features. This makes it easier to understand the relationships and impacts within the model.

3. **Intervention Capabilities**: Enable targeted interventions on a model's transcoder features based on insights gained from the attribution graph. You can modify features to specific values and observe how the model's output changes in response.

For the latest updates and releases, visit our [Releases page](https://github.com/tahmid0600/circuit-tracer/releases).

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Installation

To get started with Circuit Tracer, follow these simple steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/tahmid0600/circuit-tracer.git
   ```

2. Navigate to the project directory:
   ```bash
   cd circuit-tracer
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. You are now ready to use Circuit Tracer! 

## Usage

One quick way to start is to try our [tutorial notebook](https://github.com/tahmid0600/circuit-tracer/notebooks/tutorial.ipynb). This notebook provides step-by-step instructions to help you understand how to use the library effectively.

### Example Workflow

1. **Load Your Model**: Begin by loading a pre-trained model that contains MLP transcoders.

   ```python
   from circuit_tracer import load_model
   model = load_model('your_model_path')
   ```

2. **Find the Attribution Graph**: Use the library's functions to compute the attribution graph.

   ```python
   from circuit_tracer import find_attribution_graph
   graph = find_attribution_graph(model)
   ```

3. **Visualize the Graph**: Visualize the resulting graph to understand the connections between features.

   ```python
   from circuit_tracer import visualize_graph
   visualize_graph(graph)
   ```

4. **Perform Interventions**: Modify transcoder features and observe the changes in output.

   ```python
   from circuit_tracer import intervene_on_features
   output = intervene_on_features(model, feature_values)
   ```

## Features

- **CircuitDiscovery**: Automatically find and analyze the attribution graph of your model's transcoders.

- **Interactive Visualization**: Visualize complex relationships in the model with user-friendly graphs. Annotate features for better understanding.

- **Custom Interventions**: Change the values of transcoder features to see how these changes affect the model's output. This helps in understanding the model's behavior.

- **Extensive Documentation**: Comprehensive guides and tutorials are available to help you get started quickly.

- **Community Support**: Join our community for discussions, questions, and sharing insights.

## Contributing

We welcome contributions from the community. If you would like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/YourFeature
   ```
3. Make your changes and commit them:
   ```bash
   git commit -m "Add your feature description"
   ```
4. Push to your branch:
   ```bash
   git push origin feature/YourFeature
   ```
5. Open a pull request.

Please ensure that your code follows the existing style and includes appropriate tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or feedback, please reach out via the following channels:

- **GitHub Issues**: Use the [issues page](https://github.com/tahmid0600/circuit-tracer/issues) for bug reports or feature requests.
- **Email**: You can contact the maintainers at example@example.com.

Thank you for your interest in Circuit Tracer! We look forward to your contributions and insights.

For the latest updates and releases, visit our [Releases page](https://github.com/tahmid0600/circuit-tracer/releases).