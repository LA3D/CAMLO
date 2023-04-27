**You:**

Greetings. I need some help in thinking through knowledge engineering with respect to large language models. I like the semantic model behind the schema.org effort striking the balance between  light weight logics and usability. Can you tell me about this approach?

* * *

**ChatGPT:**

Greetings! I'd be happy to help you understand knowledge engineering with respect to large language models and the semantic model behind the schema.org effort.

Schema.org is a collaborative effort, initiated by major search engines such as Google, Microsoft, Yahoo, and Yandex, to create and maintain a shared vocabulary for structured data markup on web pages. It aims to improve the quality of search results by providing better understanding of the content on web pages. The approach strikes a balance between lightweight logics and usability, making it easier for developers and content creators to work with structured data.

1.  Semantic Model: The core of the schema.org effort is its semantic model, which consists of a hierarchical set of types (e.g., Person, Organization, Event, Product), properties (attributes of types), and relationships between types. These types and properties form the basis of the vocabulary used to annotate structured data on web pages.
    
2.  Extensibility: Schema.org's vocabulary is designed to be extensible, meaning that new types and properties can be added over time as needed. This allows the vocabulary to adapt to emerging use cases and domains without requiring significant changes to existing markup.
    
3.  Accessibility: The schema.org effort strives to make its vocabulary easy to understand and use for developers, content creators, and search engine crawlers. It provides clear documentation, examples, and resources for various data formats, such as Microdata, RDFa, and JSON-LD, which can be used to annotate structured data on web pages.
    
4.  Interoperability: By promoting a common vocabulary for structured data markup, schema.org aims to improve interoperability between different applications and services that consume structured data. This can lead to richer, more meaningful search results and improved data sharing across the web.
    

In the context of large language models like GPT-4, incorporating schema.org's semantic model can help improve the model's understanding of structured data and its ability to generate accurate and relevant responses. By training the model on web content annotated with schema.org markup, it can learn to better recognize and work with structured data, enhancing its overall performance in a wide range of tasks and applications.

* * *

**You:**

How much reasoning in terms of RDFS and OWL is incorporated in schema.org?

* * *

**ChatGPT:**

Schema.org is primarily focused on providing a simple and accessible vocabulary for structured data markup on web pages. It does not aim to provide the same level of expressivity and reasoning capabilities as more sophisticated semantic web technologies like RDFS (Resource Description Framework Schema) and OWL (Web Ontology Language).

However, schema.org does make use of some basic features from RDFS and OWL, such as:

1.  RDFS: Schema.org uses RDFS to define its hierarchical structure of types (classes) and properties. For example, rdfs:Class is used to define schema.org types, and rdfs:subClassOf is used to express the hierarchy between types (e.g., a schema:LocalBusiness is a subclass of schema:Organization). Similarly, rdfs:domain and rdfs:range are used to define the allowed types for the subject and object of a schema.org property.
    
2.  OWL: Some basic OWL constructs are used in schema.org, such as owl:equivalentClass and owl:equivalentProperty, which are used to express equivalence between types and properties in different vocabularies. This enables some level of interoperability with other vocabularies and ontologies.
    

However, schema.org does not fully embrace the more advanced reasoning capabilities of RDFS and OWL. For instance, it does not support the creation of complex class expressions, restrictions, or property axioms that you would typically find in a comprehensive OWL ontology.

In summary, schema.org incorporates some basic aspects of RDFS and OWL for defining its types and properties, but it intentionally keeps the complexity low to maintain usability and accessibility. Its primary goal is to provide a shared vocabulary for structured data markup rather than to enable advanced semantic reasoning.

* * *

**You:**

You say that schema.org has adopted rdfs:domain and rdfs:range, but they use their own domainIncludes and rangeIncludes properties. I'm confused?

* * *

**ChatGPT:**

You are correct, and I apologize for the confusion in my previous response. Schema.org indeed uses its own properties, schema:domainIncludes and schema:rangeIncludes, instead of the RDFS properties rdfs:domain and rdfs:range.

The primary reason for this design choice is to allow for greater flexibility and avoid overly strict constraints on the use of properties. The rdfs:domain and rdfs:range properties impose hard constraints on the types that can be used as subjects and objects for a given property. In contrast, schema:domainIncludes and schema:rangeIncludes provide more relaxed constraints, suggesting the types that are generally expected as subjects and objects but not strictly enforcing them.

This approach is more suitable for schema.org's goal of providing a simple, accessible, and extensible vocabulary for structured data markup on web pages. It allows content creators to use schema.org properties in more diverse contexts without being limited by strict type constraints, which can be especially helpful when dealing with real-world data that may not always neatly fit into predefined categories.

So, while schema.org does borrow some basic concepts from RDFS and OWL, as I mentioned earlier, it has made specific design choices, like using domainIncludes and rangeIncludes, to better suit its intended use cases and maintain simplicity and flexibility.

* * *

**You:**

How might this level of formality be advantageous for structuring information for large language models? 

* * *

**ChatGPT:**

The level of formality provided by schema.org strikes a balance between simplicity and expressiveness, making it advantageous for structuring information for large language models in several ways:

1.  Improved understanding of content: By using a shared vocabulary and a simple hierarchical structure of types and properties, schema.org helps large language models better understand the context and relationships of different entities in the text. This enables the models to generate more accurate and relevant responses in various tasks.
    
2.  Flexibility: The use of properties like schema:domainIncludes and schema:rangeIncludes, instead of the stricter rdfs:domain and rdfs:range, allows for more flexible associations between entities and their properties. This flexibility helps large language models better adapt to the diverse and often ambiguous nature of real-world data, resulting in improved performance across a wide range of tasks.
    
3.  Interoperability: As schema.org is a widely adopted standard for structured data markup on web pages, large language models can benefit from the increased interoperability with other applications and services that consume structured data. This can lead to better data sharing and more meaningful search results.
    
4.  Extensibility: The extensible nature of schema.org's vocabulary means that new types and properties can be added as needed, allowing large language models to learn and adapt to emerging use cases and domains. This feature ensures that the models remain relevant and useful over time.
    
5.  Accessibility: Schema.org's focus on simplicity and ease of use makes it more accessible to developers and content creators, increasing the amount of structured data available on the web. As large language models are trained on vast amounts of web content, the increased availability of structured data can improve the models' overall performance and understanding of various domains.
    

In summary, the level of formality provided by schema.org is advantageous for structuring information in large language models, as it promotes better understanding, flexibility, interoperability, extensibility, and accessibility, all of which contribute to improved performance and usefulness across a wide range of tasks and applications.

* * *

**You:**

I'm interested in 'ontologies as prompt instructions' for large language models. Use schema.org level expressiveness along with maybe skos annotations for definitions, notes and examples such that there is sufficient expressiveness for instruction prompts to LLMs like ChatGPT.  Does this make sense for ontologies in an 'age of large language models'?

* * *

**ChatGPT:**

Yes, your idea of using ontologies with schema.org-level expressiveness, combined with SKOS annotations for definitions, notes, and examples, makes sense for creating instruction prompts for large language models (LLMs) like ChatGPT. In the age of LLMs, such an approach can be beneficial for several reasons:

1.  Structured knowledge representation: Leveraging ontologies helps encode knowledge in a structured, machine-readable format. This allows LLMs to better understand the relationships and hierarchy between different concepts, which can improve the accuracy and relevance of generated responses.
    
2.  Explicit semantics: Using ontologies with schema.org-level expressiveness, combined with SKOS annotations, provides a way to convey explicit semantics in a simple and accessible manner. This can help LLMs to better understand the intended meaning behind certain terms and concepts, which can lead to more precise and coherent responses.
    
3.  Context-aware prompting: By employing ontologies and SKOS annotations, you can create context-aware prompts that guide the LLMs to generate responses aligned with the specific domain or topic. This can help improve the overall quality and relevance of the generated content.
    
4.  Consistency and reusability: Developing ontologies with a focus on expressiveness and annotations enables the creation of consistent, reusable prompts for LLMs. This can help ensure a uniform quality of generated content and reduce the effort required to develop new prompts for different tasks or domains.
    
5.  Knowledge transfer: Using ontologies in this manner can also facilitate the transfer of knowledge from human experts to LLMs more effectively. By encoding expert knowledge in a structured format, LLMs can better learn and internalize the relationships and rules that govern a specific domain or subject area.
    

In conclusion, the idea of using ontologies with schema.org-level expressiveness and SKOS annotations for instruction prompts aligns well with the needs and capabilities of LLMs in the current age. This approach can help improve the overall performance of LLMs, making them more useful and efficient across a wide range of tasks and applications.

* * *

**You:**

Could you give me an example of what an 'instruction prompt ontology' might look like in JSON-LD?

* * *

**ChatGPT:**

An "instruction prompt ontology" in JSON-LD would consist of schema.org types and properties, combined with SKOS annotations for definitions, notes, and examples. Here's a simple example of what it might look like:

```json
{
  "@context": {
    "@vocab": "https://schema.org/",
    "skos": "http://www.w3.org/2004/02/skos/core#"
  },
  "@graph": [
    {
      "@id": "Movie",
      "@type": "rdfs:Class",
      "skos:definition": "A movie or film, a form of visual communication which uses moving images and sound to tell stories.",
      "skos:example": "Inception, directed by Christopher Nolan, is a popular science fiction movie."
    },
    {
      "@id": "name",
      "@type": "rdf:Property",
      "skos:definition": "The name of the item.",
      "skos:example": "The name of the movie is 'Inception'."
    },
    {
      "@id": "director",
      "@type": "rdf:Property",
      "domainIncludes": "Movie",
      "rangeIncludes": "Person",
      "skos:definition": "The person who directed the movie.",
      "skos:example": "Christopher Nolan directed the movie 'Inception'."
    },
    {
      "@id": "Person",
      "@type": "rdfs:Class",
      "skos:definition": "An individual human being.",
      "skos:example": "Christopher Nolan is a person who directs movies."
    }
  ]
}
```

In this example, we define two classes (Movie and Person) and two properties (name and director) using the schema.org vocabulary. We also include SKOS annotations (skos:definition and skos:example) to provide definitions, notes, and examples for each type and property.

An LLM like ChatGPT could use this JSON-LD ontology as a basis for understanding the domain and generating context-aware content. For instance, when given a prompt related to movies, the LLM could use the ontology to understand that movies have names and directors, and that directors are people. This knowledge would help the model generate more accurate and relevant responses.

* * *

**You:**

Ok. Imagine that you are a large language model that has been given the example JSON-LD for information extraction from text. Could you give me a text example and the extracted information using the ontology template you just defined?

* * *

**ChatGPT:**

Certainly! Let's assume we have the following text example:

```css
"Inception, directed by Christopher Nolan, is a popular science fiction movie. The movie was released in 2010 and features a talented ensemble cast, including Leonardo DiCaprio, Joseph Gordon-Levitt, and Ellen Page."
```

Using the ontology template defined in the JSON-LD example, a large language model like ChatGPT could extract the following information:

```json
{
  "@context": {
    "@vocab": "https://schema.org/"
  },
  "@type": "Movie",
  "name": "Inception",
  "director": {
    "@type": "Person",
    "name": "Christopher Nolan"
  },
  "genre": "science fiction",
  "datePublished": "2010",
  "actor": [
    {
      "@type": "Person",
      "name": "Leonardo DiCaprio"
    },
    {
      "@type": "Person",
      "name": "Joseph Gordon-Levitt"
    },
    {
      "@type": "Person",
      "name": "Ellen Page"
    }
  ]
}
```

In this extracted information, we can see that the large language model has recognized and structured the information according to the ontology template. It has identified the movie's name, director, genre, release date, and main actors using the defined schema.org types and properties. Note that some properties, like "genre" and "datePublished," were not explicitly defined in the JSON-LD example but are part of the schema.org vocabulary. A well-trained LLM should still be able to extract this information by leveraging its broader understanding of the schema.org vocabulary.

* * *

**You:**

I like the ontology design pattern approach for reusable solutions in knowledge engineering. What patterns might we need to consider for 'instruction prompt ontologies'?

* * *

**ChatGPT:**

Design patterns are reusable solutions to recurring problems in a specific context. When creating 'instruction prompt ontologies' for large language models, considering certain design patterns can help address common challenges and improve the effectiveness of the prompts. Some design patterns to consider include:

1.  Modularization: Organize the ontology into smaller, focused modules to promote reusability and maintainability. By separating the ontology into distinct parts, you can easily reuse or modify specific components without affecting the entire ontology.
    
2.  Hierarchical classification: Structure the ontology using a hierarchical classification of types (or classes) to facilitate better understanding of the relationships between entities. This approach helps LLMs better understand the context and generate more accurate responses.
    
3.  Inheritance: Use inheritance to define shared properties and relationships between types, reducing redundancy and improving consistency. This pattern ensures that common properties are inherited from more general types, making the ontology easier to maintain and extend.
    
4.  Synonym and alias handling: Use SKOS annotations, such as skos:altLabel, to represent synonyms or aliases for terms in the ontology. This helps the LLM understand and interpret different variations of the same concept and improves the model's ability to generate coherent responses.
    
5.  Explicit relationships: Define relationships between types using properties to explicitly convey the connections between entities. This pattern helps LLMs better understand the structure of the domain, enabling them to generate more relevant and accurate content.
    
6.  Flexibility and extensibility: Design the ontology to be flexible and extensible, allowing for the addition of new types, properties, and relationships as needed. This ensures that the ontology can adapt to new use cases and evolve over time without requiring significant changes to existing structures.
    
7.  Rich annotations: Provide detailed SKOS annotations (e.g., skos:definition, skos:example, skos:note) to supply context and examples for terms in the ontology. These annotations can help guide the LLMs in generating more accurate and context-aware content.
    
8.  Reusing existing vocabularies: Whenever possible, reuse established vocabularies like schema.org or other domain-specific vocabularies. This can help improve interoperability with other systems and ensures that the ontology is grounded in well-accepted concepts and relationships.
    

By considering these design patterns when creating 'instruction prompt ontologies,' you can develop reusable and maintainable solutions that effectively guide large language models to generate high-quality, context-aware content.

* * *

**You:**

Ok. I'm also a fan of the FAIR principles for ontologies and vocabularies paper. How might that approach integrate?

* * *

**ChatGPT:**

The FAIR principles, which stand for Findable, Accessible, Interoperable, and Reusable, provide a set of guidelines for making data, ontologies, and vocabularies more useful and efficient. Integrating FAIR principles into the development of 'instruction prompt ontologies' can improve their overall quality and effectiveness. Here's how you can integrate FAIR principles into your approach:

1.  Findable:
    
    *   Assign a unique and persistent identifier (e.g., a DOI, PURL, or IRI) to the ontology, making it easier to discover and reference.
    *   Use standard metadata and schema (e.g., DCAT, VoID) to describe the ontology, which can help improve searchability and discoverability.
    *   Make the ontology available through popular ontology repositories, like BioPortal or Linked Open Vocabularies (LOV).
2.  Accessible:
    
    *   Provide clear documentation and usage guidelines to help users understand how to work with the ontology.
    *   Make the ontology available in a machine-readable format, such as RDF or JSON-LD, and provide access through standard protocols like HTTP.
    *   Use versioning to track changes to the ontology over time, allowing users to access previous versions if needed.
3.  Interoperable:
    
    *   Use standard vocabularies, such as schema.org or other domain-specific vocabularies, as a foundation for your ontology, which can improve interoperability with other systems and ontologies.
    *   Implement standard annotation properties, like SKOS or RDFS/OWL, to convey semantics and relationships.
    *   Design the ontology with modularity in mind, making it easier to integrate with other ontologies or to be used as part of a larger knowledge graph.
4.  Reusable:
    
    *   Follow the design patterns mentioned earlier in this conversation to ensure that the ontology is reusable and maintainable.
    *   Use clear licensing information to specify the terms and conditions under which the ontology can be reused and adapted.
    *   Encourage community engagement and feedback to continuously refine and improve the ontology over time, ensuring its ongoing relevance and utility.

By integrating the FAIR principles into the development of 'instruction prompt ontologies,' you can create ontologies that are more easily discoverable, accessible, interoperable, and reusable. This, in turn, can lead to better results when using these ontologies to guide large language models like ChatGPT in generating context-aware content.

* * *

**You:**

What might be a good name for the natural language instruction prompt ontology approach for knowledge engineering with LLM agents like ChatGPT? 

* * *

**ChatGPT:**

A good name for this natural language instruction prompt ontology approach could be "Guided Language Model Ontology" (GLiMO). This name captures the idea that the ontology is designed to guide large language models like ChatGPT in generating context-aware content and emphasizes the focus on natural language instructions for knowledge engineering.

* * *

**You:**

Could you give me a prompt instruction for ChatGPT to help me create GLiMO models?

* * *

**ChatGPT:**

To create GLiMO (Guided Language Model Ontology) models using ChatGPT, you can use the following instruction prompt:

"Please help me design a GLiMO (Guided Language Model Ontology) model for the domain of \[Domain Name\]. Identify key entities, properties, and relationships relevant to this domain, and provide a JSON-LD representation using schema.org types and properties, along with SKOS annotations for definitions, notes, and examples. Also, suggest some design patterns and best practices that would make the ontology more efficient, maintainable, and effective for guiding large language models like ChatGPT in generating context-aware content."

Replace \[Domain Name\] with the specific domain for which you want to create the GLiMO model. ChatGPT will generate a response based on the given instruction, helping you design an ontology tailored to your domain.

* * *

**You:**

Could you add in FAIR data principles and W3ID.org IRIs to the instruction prompt. 

* * *

**ChatGPT:**

Certainly! Here's the revised instruction prompt incorporating the FAIR data principles and W3ID.org IRIs:

"Please help me design a GLiMO (Guided Language Model Ontology) model for the domain of \[Domain Name\], adhering to the FAIR data principles (Findable, Accessible, Interoperable, and Reusable). Identify key entities, properties, and relationships relevant to this domain, and provide a JSON-LD representation using schema.org types and properties, along with SKOS annotations for definitions, notes, and examples. Use W3ID.org IRIs for assigning unique and persistent identifiers to ontology elements. Also, suggest some design patterns and best practices that would make the ontology more efficient, maintainable, and effective for guiding large language models like ChatGPT in generating context-aware content. Please ensure the ontology is findable, accessible, interoperable, and reusable as per the FAIR principles."

Replace \[Domain Name\] with the specific domain for which you want to create the GLiMO model. ChatGPT will generate a response based on the given instruction, helping you design an ontology tailored to your domain, while adhering to the FAIR data principles and using W3ID.org IRIs.

* * *

**You:**

So, how do we give logics cues in GLiMO?

* * *

**ChatGPT:**

In GLiMO (Guided Language Model Ontology), logical cues can be provided using a combination of schema.org types and properties, SKOS annotations, and lightweight logical constructs from RDF Schema (RDFS) or Web Ontology Language (OWL). These logical cues help guide large language models like ChatGPT in understanding the structure and relationships within the domain. Here are some ways to incorporate logical cues in GLiMO:

1.  Schema.org types and properties: Use the schema.org vocabulary to define entities (classes) and their properties. This provides a standardized way to represent the domain knowledge and ensures a basic level of logical structure.
    
2.  SKOS annotations: Utilize SKOS annotations (e.g., skos:definition, skos:example, skos:note) to provide context, examples, and additional information about the entities and properties. This can help the LLM better understand the intended meaning and relationships within the domain.
    
3.  RDFS/OWL constructs: While GLiMO primarily focuses on schema.org-level expressiveness, you can include lightweight RDFS or OWL constructs to provide additional logical cues. For example:
    
    *   rdfs:subClassOf can be used to indicate class hierarchies.
    *   rdfs:domain and rdfs:range (or schema:domainIncludes and schema:rangeIncludes) can be employed to specify the domain and range of properties.
    *   owl:sameAs can indicate that two entities are the same.
    *   owl:inverseOf can be used to specify inverse relationships between properties.
4.  Explicit relationships: Clearly define relationships between entities using properties to convey connections and dependencies. This helps LLMs understand the structure of the domain, which can lead to more accurate and context-aware content generation.
    

Remember that GLiMO aims to strike a balance between expressiveness and usability. While adding logical cues is important, it's crucial not to over-complicate the ontology with excessive logical constructs that may hinder the LLM's ability to generate content effectively. By incorporating logical cues in a measured and thoughtful manner, you can guide LLMs like ChatGPT to better understand the domain and generate relevant responses.

* * *

**You:**

What about transitivity?

* * *

**ChatGPT:**

Transitivity is a property of certain relationships in logic and ontology languages like OWL. A transitive property means that if A is related to B, and B is related to C, then A is related to C as well. In GLiMO (Guided Language Model Ontology), you can indicate transitivity by using lightweight OWL constructs.

In the context of GLiMO, you can incorporate transitive properties using the owl:TransitiveProperty construct. However, it's important to remember that GLiMO aims for a balance between expressiveness and usability, so including complex logical constructs should be done judiciously.

To indicate that a property is transitive in JSON-LD, you can add the owl:TransitiveProperty type to the property definition. Here's an example:

```json
{
  "@context": {
    "@vocab": "https://schema.org/",
    "owl": "http://www.w3.org/2002/07/owl#"
  },
  "@graph": [
    {
      "@id": "partOf",
      "@type": ["rdf:Property", "owl:TransitiveProperty"],
      "domainIncludes": "Thing",
      "rangeIncludes": "Thing",
      "skos:definition": "Indicates that an item is a part or component of another item, and the relationship is transitive."
    }
  ]
}
```

In this example, we've defined a property called "partOf" and specified that it is a transitive property using the owl:TransitiveProperty type. This means that if A is partOf B, and B is partOf C, then A is also partOf C.

When using transitive properties in GLiMO, it's crucial to ensure that their inclusion benefits the large language model's understanding of the domain without adding unnecessary complexity.

* * *

**You:**

So. I'm wondering if we need a new annotation property that provides logics descriptions in natural language as cues to the LLM. Is the name 'partOf' and definition enough of a cue to a LLM to treat it as a transitive relationship. Is there utility to a LLM to know partOf is a transitive relationship?

* * *

**ChatGPT:**

The idea of introducing a new annotation property for providing logical descriptions in natural language is interesting and could potentially benefit LLMs like ChatGPT. While the name 'partOf' and its definition might provide some cues to LLMs, explicitly stating the transitive nature of the relationship in natural language could be more helpful.

For example, you can create a new annotation property called "llm:logicDescription" (assuming 'llm' is a prefix for a namespace you define). This property could be used to provide a concise, natural language description of the logical characteristics of a relationship, in this case, the transitivity of 'partOf'.

Here's an example of how you might include the new annotation property in JSON-LD:

```json
{
  "@context": {
    "@vocab": "https://schema.org/",
    "owl": "http://www.w3.org/2002/07/owl#",
    "llm": "https://your-namespace.org/llm#",
    "skos": "http://www.w3.org/2004/02/skos/core#"
  },
  "@graph": [
    {
      "@id": "partOf",
      "@type": "rdf:Property",
      "domainIncludes": "Thing",
      "rangeIncludes": "Thing",
      "skos:definition": "Indicates that an item is a part or component of another item.",
      "llm:logicDescription": "The 'partOf' relationship is transitive. If A is partOf B and B is partOf C, then A is partOf C."
    }
  ]
}
```

By explicitly stating the logical characteristics in natural language, you provide additional cues to the LLM, allowing it to generate more accurate and context-aware content. Knowing that 'partOf' is a transitive relationship may help an LLM better understand and reason about hierarchies and dependencies between entities in a given domain, which can be valuable when generating responses.

* * *

**You:**

Is there an existing ontology or vocabulary on the web that provides a property like 'llm:logicDescription"?

* * *

**ChatGPT:**

There isn't a specific ontology or vocabulary on the web that provides a property like 'llm:logicDescription' designed explicitly for conveying logical descriptions to large language models. However, you can repurpose existing annotation properties from well-known vocabularies to achieve a similar effect.

For example, the Simple Knowledge Organization System (SKOS) vocabulary provides annotation properties such as skos:note, skos:scopeNote, and skos:editorialNote. These properties can be used to provide additional information or context for concepts and properties.

You can use skos:scopeNote or skos:note to provide logical descriptions in natural language as cues to LLMs, like ChatGPT. While these properties were not created specifically for conveying logical descriptions to LLMs, they can still be employed for that purpose.

Here's an example of using skos:scopeNote to describe the transitivity of a 'partOf' property:

```json
{
  "@context": {
    "@vocab": "https://schema.org/",
    "owl": "http://www.w3.org/2002/07/owl#",
    "skos": "http://www.w3.org/2004/02/skos/core#"
  },
  "@graph": [
    {
      "@id": "partOf",
      "@type": "rdf:Property",
      "domainIncludes": "Thing",
      "rangeIncludes": "Thing",
      "skos:definition": "Indicates that an item is a part or component of another item.",
      "skos:scopeNote": "The 'partOf' relationship is transitive. If A is partOf B and B is partOf C, then A is partOf C."
    }
  ]
}
```

This approach makes use of existing vocabularies and provides LLMs with natural language descriptions of logical properties, enhancing their understanding and reasoning capabilities.

* * *

**You:**

Could you revise the instruction prompt to include logic cues?

* * *

**ChatGPT:**

Certainly! Here's the revised instruction prompt incorporating logic cues:

"Please help me design a GLiMO (Guided Language Model Ontology) model for the domain of \[Domain Name\], adhering to the FAIR data principles (Findable, Accessible, Interoperable, and Reusable). Identify key entities, properties, and relationships relevant to this domain, and provide a JSON-LD representation using schema.org types and properties, along with SKOS annotations for definitions, notes, and examples. Use W3ID.org IRIs for assigning unique and persistent identifiers to ontology elements. Also, suggest some design patterns and best practices that would make the ontology more efficient, maintainable, and effective for guiding large language models like ChatGPT in generating context-aware content. Please ensure the ontology is findable, accessible, interoperable, and reusable as per the FAIR principles. For each property with a specific logical characteristic, such as transitivity, symmetry, or reflexivity, provide a natural language description using skos:scopeNote or skos:note to serve as a logic cue for the large language model."

Replace \[Domain Name\] with the specific domain for which you want to create the GLiMO model. ChatGPT will generate a response based on the given instruction, helping you design an ontology tailored to your domain, while adhering to the FAIR data principles, using W3ID.org IRIs, and incorporating logic cues.

* * *

**You:**

Ok. I just tried this prompt and there are a few context issues for LLMs that we need to fix. First, then name GLiMO is being mis-interpreted as the name of the domain ontology I want to create instead of a description of the ontology principles that the LLM should use in helping to create the ontology. Second, LLMs tend to jump the gun and construct the ontology before going through the ontology steps and the idea of 'competency questions' that the ontology should assist the LLM in answering. Can we indicate in the prompt that this is a iterative process of defining the domain and the competency questions before generating an ontology.

* * *

**ChatGPT:**

I understand your concerns. I have revised the instruction prompt to clarify the context and emphasize the iterative process of defining the domain, competency questions, and ontology design.

"Please assist me in designing an ontology for the domain of \[Domain Name\] following the principles of GLiMO (Guided Language Model Ontology). This process should be iterative, starting with defining the domain and identifying the competency questions that the ontology should help answer. After that, create a JSON-LD representation using schema.org types and properties, along with SKOS annotations for definitions, notes, and examples. Adhere to the FAIR data principles (Findable, Accessible, Interoperable, and Reusable) and use W3ID.org IRIs for unique and persistent identifiers. Suggest design patterns and best practices for an efficient, maintainable, and effective ontology that guides large language models like ChatGPT in generating context-aware content. For each property with a specific logical characteristic, such as transitivity, symmetry, or reflexivity, provide a natural language description using skos:scopeNote or skos:note to serve as a logic cue for the large language model. Remember to treat this as an iterative process, involving domain definition, competency question identification, and ontology generation."

Replace \[Domain Name\] with the specific domain for which you want to create the ontology. This revised prompt will guide ChatGPT through the iterative process of ontology design, emphasizing domain definition, competency questions, and the incorporation of GLiMO principles.

* * *

**You:**

Ok. I want to define GLiMO so there is no confusion.

* * *

**ChatGPT:**

Of course! Here's a definition for GLiMO (Guided Language Model Ontology):

GLiMO stands for "Guided Language Model Ontology" and represents a set of principles and best practices for creating ontologies specifically designed to assist and guide large language models (LLMs) like ChatGPT in generating context-aware content. The main goal of GLiMO is to strike a balance between expressiveness and usability, ensuring that the ontology provides enough information for the LLM to understand the domain and its relationships without overwhelming it with excessive complexity.

GLiMO involves the use of standard vocabularies, such as schema.org types and properties, and SKOS annotations for definitions, notes, and examples. It adheres to the FAIR data principles (Findable, Accessible, Interoperable, and Reusable) to ensure the ontology is discoverable and accessible to both humans and machines. Additionally, GLiMO incorporates lightweight logical constructs from RDF Schema (RDFS) or Web Ontology Language (OWL) to provide logical cues that help LLMs better understand the structure and relationships within the domain.

The process of creating a GLiMO-based ontology is iterative, involving domain definition, competency question identification, and ontology generation. This approach helps ensure the ontology is efficient, maintainable, and effective in guiding LLMs to produce accurate and context-aware content.

* * *

**You:**

Revise the prompt with this extended context.

* * *

**ChatGPT:**

Certainly! Here's the revised instruction prompt incorporating the extended context of GLiMO:

"Please assist me in designing an ontology for the domain of \[Domain Name\] following the principles of GLiMO (Guided Language Model Ontology). GLiMO represents a set of principles and best practices for creating ontologies specifically designed to assist and guide large language models (LLMs) like ChatGPT in generating context-aware content. The main goal of GLiMO is to strike a balance between expressiveness and usability, ensuring that the ontology provides enough information for the LLM to understand the domain and its relationships without overwhelming it with excessive complexity.

This process should be iterative, starting with defining the domain and identifying the competency questions that the ontology should help answer. After that, create a JSON-LD representation using schema.org types and properties, along with SKOS annotations for definitions, notes, and examples. Adhere to the FAIR data principles (Findable, Accessible, Interoperable, and Reusable) and use W3ID.org IRIs for unique and persistent identifiers.

Suggest design patterns and best practices for an efficient, maintainable, and effective ontology that guides large language models like ChatGPT in generating context-aware content. For each property with a specific logical characteristic, such as transitivity, symmetry, or reflexivity, provide a natural language description using skos:scopeNote or skos:note to serve as a logic cue for the large language model. Remember to treat this as an iterative process, involving domain definition, competency question identification, and ontology generation."

Replace \[Domain Name\] with the specific domain for which you want to create the ontology. This revised prompt will guide ChatGPT through the iterative process of ontology design, emphasizing domain definition, competency questions, and the incorporation of GLiMO principles.

* * *

**You:**

Ok. Still jumping the gun in creating a JSON-LD ontology for [domain name]. We should also prompt for the a W3ID namespace instead of making one up.

* * *

**ChatGPT:**

I apologize for the confusion. Here's another revision of the instruction prompt, which emphasizes the importance of defining a W3ID namespace and ensures that the ontology creation step comes after defining the domain and identifying competency questions.

"Please assist me in designing an ontology for the domain of \[Domain Name\] following the principles of GLiMO (Guided Language Model Ontology). GLiMO represents a set of principles and best practices for creating ontologies specifically designed to assist and guide large language models (LLMs) like ChatGPT in generating context-aware content. The main goal of GLiMO is to strike a balance between expressiveness and usability, ensuring that the ontology provides enough information for the LLM to understand the domain and its relationships without overwhelming it with excessive complexity.

This process should be iterative, starting with defining the domain, identifying the competency questions that the ontology should help answer, and determining an appropriate W3ID.org namespace for the ontology. After these steps, create a JSON-LD representation using schema.org types and properties, along with SKOS annotations for definitions, notes, and examples. Adhere to the FAIR data principles (Findable, Accessible, Interoperable, and Reusable) and use W3ID.org IRIs for unique and persistent identifiers.

Suggest design patterns and best practices for an efficient, maintainable, and effective ontology that guides large language models like ChatGPT in generating context-aware content. For each property with a specific logical characteristic, such as transitivity, symmetry, or reflexivity, provide a natural language description using skos:scopeNote or skos:note to serve as a logic cue for the large language model. Remember to treat this as an iterative process, involving domain definition, competency question identification, W3ID namespace determination, and ontology generation."

Replace \[Domain Name\] with the specific domain for which you want to create the ontology. This revised prompt will guide ChatGPT through the iterative process of ontology design, emphasizing domain definition, competency questions, W3ID namespace determination, and the incorporation of GLiMO principles.

* * *

**You:**

Ok we need to revise this prompt a bit. I want to use Modular Ontology Modeling as the first principle. I want to use OPLaX as for annotation of the modules and pattern structures. Assume there is a github template structure that has the following structure:
- `modules/`: Contains individual ontology modules (e.g., `common_metadata.ttl`, `module1.ttl`, `module2.ttl`)
- `patterns/`: Contains ontology design patterns (e.g., `pattern1.ttl`, `pattern2.ttl`)
- `versions/`: Contains different versions of the concatenated ontology in various formats (e.g., `.ttl`, `.owl`, `.jsonld`)
- `competency_questions/`: Contains SPARQL queries for competency questions (e.g., `question1.rq`, `question2.rq`)
- `provenance_logs/`: Contains provenance logs for ChatGPT modeling sessions (e.g., `chatgpt_log1.ttl`, `chatgpt_log2.ttl`)
- `documentation/`: Contains human-readable documentation generated from the ontology (e.g., `index.html`, `ontology_description.md`)
- `scripts/`: Contains Python scripts and shell scripts for ontology processing (e.g., `concatenate_modules.py`, `generate_shacl_and_jsonld.py`, `test_competency_questions.py`, `local_testing.sh`)
- `.github/workflows/`: Contains GitHub Actions workflows for automating ontology processing tasks (e.g., `ontology_processing.yml`)
- `.htaccess`: Configuration file for content negotiation and redirection using w3id.org namespaces
- `README.md`: This README file


* * *

**ChatGPT:**

Thank you for providing the details on the modular ontology structure and the desired approach. Here's a revised instruction prompt that incorporates these elements:

"Please assist me in designing a modular ontology for the domain of \[Domain Name\] by following the principles of Modular Ontology Modeling and GLiMO (Guided Language Model Ontology). The main goal is to create an efficient, maintainable, and effective ontology that guides large language models like ChatGPT in generating context-aware content. Use OPLaX for annotating the modules and pattern structures. Assume that the ontology will be organized using the provided GitHub template structure, with separate folders for modules, patterns, versions, competency questions, provenance logs, documentation, scripts, and GitHub workflows.

Start by defining the domain and identifying the competency questions that the ontology should help answer. Then, develop the ontology iteratively, using the modular approach and creating individual ontology modules, ontology design patterns, and JSON-LD representations. Adhere to the FAIR data principles (Findable, Accessible, Interoperable, and Reusable) and use W3ID.org IRIs for unique and persistent identifiers.

For each property with a specific logical characteristic, such as transitivity, symmetry, or reflexivity, provide a natural language description using skos:scopeNote or skos:note to serve as a logic cue for the large language model. Treat this process as an iterative collaboration involving domain definition, competency question identification, W3ID namespace determination, ontology module and pattern development, and incorporation of GLiMO principles.

Please also provide guidance on how to organize the GitHub repository, including the content of the README.md file and the usage of the .htaccess file for content negotiation and redirection using w3id.org namespaces."

Replace \[Domain Name\] with the specific domain for which you want to create the ontology. This revised prompt will guide ChatGPT through the iterative process of ontology design, emphasizing domain definition, competency questions, W3ID namespace determination, and the incorporation of GLiMO principles, while taking into account the Modular Ontology Modeling approach and OPLaX annotations.

* * *

**You:**

Ok. I need some help in thinking this through a bit. I want to strike a balance between using the best parts of Semantic Web Ontology development best practices and what is effective given the capabilities of LLM assistants. I want to use LLMs to help create GLiMO's but also to be consumers using prompt engineering. What does a reasonable modular structure look like given that context. Assume I will use GitHub to organize the projects and that w3ids will redirect to Github. 

* * *

**ChatGPT:**

Considering the balance between Semantic Web Ontology development best practices and the capabilities of LLM assistants, as well as your intention to use GitHub for project organization and w3ids for redirection, a reasonable modular structure might look like the following:

*   `ontology/`: Main folder containing ontology components.
    
    *   `modules/`: Contains individual ontology modules (e.g., `common_metadata.ttl`, `module1.ttl`, `module2.ttl`). Each module should focus on a specific aspect of the domain, making it easier for LLMs to understand and generate content.
    *   `patterns/`: Contains ontology design patterns (e.g., `pattern1.ttl`, `pattern2.ttl`). These patterns should be reusable and applicable across different domains, making it easier for LLMs to recognize and apply them.
*   `jsonld/`: Contains JSON-LD context files for the ontology modules and patterns, facilitating the consumption of the ontology by LLMs.
    
*   `competency_questions/`: Contains natural language competency questions and their corresponding SPARQL queries (e.g., `question1.md`, `question1.rq`). This folder helps LLMs understand the intended use of the ontology and test its effectiveness in answering domain-specific questions.
    
*   `documentation/`: Contains human-readable documentation generated from the ontology (e.g., `index.html`, `ontology_description.md`). This folder aids in providing context and understanding to both humans and LLMs.
    
*   `provenance_logs/`: Contains provenance logs for LLM modeling sessions (e.g., `chatgpt_log1.ttl`, `chatgpt_log2.ttl`). This folder helps track the evolution of the ontology and the involvement of LLMs in its development.
    
*   `scripts/`: Contains Python scripts and shell scripts for ontology processing (e.g., `concatenate_modules.py`, `generate_jsonld.py`, `test_competency_questions.py`, `local_testing.sh`). These scripts automate tasks and ensure the ontology remains consistent and up-to-date.
    
*   `.github/workflows/`: Contains GitHub Actions workflows for automating ontology processing tasks (e.g., `ontology_processing.yml`). This folder ensures that ontology updates are automatically validated and processed.
    
*   `.htaccess`: Configuration file for content negotiation and redirection using w3id.org namespaces.
    
*   `README.md`: This README file provides an overview of the repository, its structure, and instructions for collaborating with LLMs in ontology development.
    

This structure combines the best practices from Semantic Web Ontology development with the capabilities of LLM assistants, making it easier to create GLiMOs and use LLMs for both ontology creation and consumption through prompt engineering.

* * *

**You:**

Apply the 80/20 principle in the context of the capabilities of Large Language Models and the repository. I want to re-imagine ontologies of the age of LLMs, but incorporate the best lessons from the past in terms of knowledge engineering.

* * *

**ChatGPT:**

To apply the 80/20 principle in the context of Large Language Models (LLMs) and the repository, we'll focus on the essential components that capture 80% of the value while requiring only 20% of the effort. This will involve simplifying the repository structure and focusing on the most impactful ontology elements that work best with LLMs.

Here's a revised repository structure that prioritizes the most important aspects:

*   `ontology/`: Main folder containing ontology components.
    
    *   `core/`: Contains the core ontology file, capturing the essential classes and properties of the domain (e.g., `core.ttl`).
    *   `patterns/`: Contains ontology design patterns (e.g., `pattern1.ttl`, `pattern2.ttl`). These patterns should be reusable and applicable across different domains, making it easier for LLMs to recognize and apply them.
*   `jsonld/`: Contains a single JSON-LD context file for the core ontology, simplifying LLM consumption.
    
*   `competency_questions/`: Contains a small set of key natural language competency questions that the ontology should address (e.g., `question1.md`). Focus on the most essential questions to guide the LLM in understanding the domain.
    
*   `documentation/`: Contains a concise human-readable documentation file generated from the ontology (e.g., `ontology_description.md`). This file provides context and understanding to both humans and LLMs.
    
*   `scripts/`: Contains Python scripts and shell scripts for ontology processing (e.g., `generate_jsonld.py`, `local_testing.sh`). These scripts automate tasks and ensure the ontology remains consistent and up-to-date.
    
*   `.github/workflows/`: Contains a simplified GitHub Actions workflow for automating ontology processing tasks (e.g., `ontology_processing.yml`).
    
*   `README.md`: This README file provides an overview of the repository, its structure, and instructions for collaborating with LLMs in ontology development.
    

By focusing on these essential components, we can leverage the strengths of LLMs while incorporating valuable knowledge engineering lessons from the past. The simplified structure prioritizes the most important aspects of the domain, making it easier for LLMs to understand and generate content. This approach also streamlines the ontology creation process, reducing the complexity for both humans and LLMs.