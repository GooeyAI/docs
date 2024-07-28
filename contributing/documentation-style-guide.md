# Documentation Style Guide

## **Documentation Style Guide** <a href="#id-2gidycpw9q4p" id="id-2gidycpw9q4p"></a>

To maintain industry parity, we take inspiration from the best, our Documentation Style Guide is based on [Langchain's Documentation Style Guide](https://python.langchain.com/v0.2/docs/contributing/documentation/style\_guide/#general-guidelines)

### **General guidelines**[**​**](https://python.langchain.com/v0.2/docs/contributing/documentation/style\_guide/#general-guidelines) <a href="#u06mnxhr6vqy" id="u06mnxhr6vqy"></a>

Here are guidelines for contributing and writing docs for Gooey.AI.

#### **Avoid duplication**[**​**](https://python.langchain.com/v0.2/docs/contributing/documentation/style\_guide/#avoid-duplication) <a href="#id-2bamt5jlsl9z" id="id-2bamt5jlsl9z"></a>

Multiple pages that cover the same material in depth are difficult to maintain and cause confusion. There should be only one (very rarely two), canonical pages for a given concept or feature. Instead, you should link to other guides.

#### **Link to other sections**[**​**](https://python.langchain.com/v0.2/docs/contributing/documentation/style\_guide/#link-to-other-sections) <a href="#id-227g7xprhisq" id="id-227g7xprhisq"></a>

Because sections of the docs do not exist in a vacuum, it is important to link to other sections as often as possible to allow a developer to learn more about an unfamiliar topic inline.

**This includes linking to the API references as well as conceptual sections!**

#### **Be concise**[**​**](https://python.langchain.com/v0.2/docs/contributing/documentation/style\_guide/#be-concise) <a href="#id-7trs8xwq50e2" id="id-7trs8xwq50e2"></a>

In general, take a less-is-more approach. If a section with a good explanation of a concept already exists, you should link to it rather than re-explain it, unless the concept you are documenting presents some new wrinkle.

Be concise, including in code samples.

#### **General style**[**​**](https://python.langchain.com/v0.2/docs/contributing/documentation/style\_guide/#general-style) <a href="#lvse80j7jo34" id="lvse80j7jo34"></a>

* Use active voice and present tense whenever possible
* Use examples and code snippets to illustrate concepts and usage
* Use appropriate header levels (#, ##, ###, etc.) to organize the content hierarchically
* Use fewer cells with more code to make copy/paste easier
* Use bullet points and numbered lists to break down information into easily digestible chunks
* Use tables (especially for Reference sections) and diagrams often to present information visually
* Include the table of contents for longer documentation pages to help readers navigate the content, but hide it for shorter pages
