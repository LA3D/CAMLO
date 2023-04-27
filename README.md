# CALMO: Context-Aware Language Model Ontology

CALMO (Context-Aware Language Model Ontology) is an ontology-vocabulary designed to provide context and guidance to large language models like ChatGPT, enabling them to generate more context-aware content. CALMO builds upon schema.org, Prov-O, and SKOS and leverages linked data principles to enhance the understanding of JSON key-value pairs.

## Repository Structure

- `context/`: JSON-LD context files
- `modules/`: Individual ontology modules
- `patterns/`: Ontology design patterns
- `versions/`: Different versions of the ontology
- `competency-questions/`: Competency questions that the ontology should answer
- `provenance-logs/`: Logs related to the development of the ontology, e.g., updates and changes
- `documentation/`: Detailed documentation for the ontology, including usage and examples
- `scripts/`: Utility scripts for ontology validation, conversion, and other tasks
- `.github/`: GitHub workflows for ontology management, testing, and continuous integration

## Formats

CALMO is available in both JSON-LD and Turtle formats. The JSON-LD format is designed for web developers who are more familiar with JSON and is suitable for large language models that work well with JSON data. The Turtle format is a popular and human-readable RDF syntax, favored by the Semantic Web and Linked Data communities.

## Getting Started

To use CALMO in your project, follow these steps:

1. Choose the format (JSON-LD or Turtle) that best fits your needs.
2. Download the corresponding file from the `versions/` folder or use the w3id.org identifiers to reference the ontology.
3. Include the ontology in your application as needed, and follow the documentation for guidance on how to use the ontology to provide context and guidance to your language models.

## Documentation

Please refer to the `documentation/` folder for detailed documentation on CALMO, including usage examples and explanations of the ontology concepts, properties, and relationships.

## Contributing

We welcome contributions to CALMO! If you'd like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your changes.
3. Commit your changes to the branch.
4. Create a pull request, and provide a detailed description of your changes.

Before submitting a pull request, please ensure that your changes follow the existing ontology structure and guidelines.

## License

This project is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/). You are free to share and adapt the material, as long as you give appropriate credit, provide a link to the license, and indicate if changes were made.
