# GitHub README Tone Guide

## Style Elements
- Use UK English spellings and grammar.
- Write in clear, approachable language that balances technical accuracy with accessibility.
- Use present tense for describing functionality and features.
- Employ active voice for instructions and recommendations.
- Keep sentences concise and direct.
- Use informative headers that describe content rather than generic labels.
- Maintain consistent terminology throughout - avoid synonyms for technical terms.
- Use code formatting for all code examples, commands, file paths, and configuration elements.
- Format content in Markdown.
- Use "we" rather than "I" when referring to the project maintainers.
- Avoid contractions in formal sections, but they can be used in more conversational sections.
- When explaining software processes, use pythonic pseudocode with 4-space indentation (not tabs).
- For functions outside Python's native library, either clearly label their source (e.g., math.sqrt()) or create self-explanatory function names (e.g., validate_network_configuration()).

## Emotional Tone
- Project enthusiasm for the project without marketing hyperbole.
- Maintain a helpful, community-oriented voice.
- Be confident about project capabilities without overpromising.
- Acknowledge limitations or work-in-progress areas honestly.
- Focus on problem-solving rather than self-promotion.
- Express gratitude for contributions and community involvement.
- Use analogies when they clarify complex concepts, but keep them relevant to technical users.

## Document Structure
- Begin with a clear, concise project name and one-line description.
- Include essential badges (build status, version, license, etc.) near the top.
- Provide a Table of Contents for READMEs longer than one screen.
- Organize in descending order of importance - most critical information first.
- Use the following sections as appropriate:
  - Quick Start/Installation
  - Features/Capabilities
  - Usage Examples
  - API Documentation
  - Configuration
  - Requirements/Prerequisites
  - Contributing Guidelines
  - License Information
  - Acknowledgements
- Use paragraphs rather than bullet points for explanations where appropriate.
- Keep paragraphs short (2-3 sentences) to break up ideas into key concepts.

## Phrases to Use
- "This project helps you..."
- "To get started:"
- "Here's a simple example:"
- "You might find it useful when..."
- "Contributions are welcome"
- "For more details, see the [documentation]"
- "Our measurements show..."
- "Based on our testing..."

## Phrases to Avoid
- "Best-in-class" or "industry-leading" (marketing language)
- "Simply" or "just" (minimizes complexity)
- "Easy to use" (subjective judgment)
- "Obviously" or "clearly" (presumptuous)
- "Revolutionary" or "game-changing" (hyperbolic)
- Excessive exclamation marks or all-caps emphasis
- "In the ever changing world of cloud networks" (cliché)

## Visual Elements
- Use descriptive alt text for all images and screenshots.
- Include animated GIFs for demonstrating workflows where helpful.
- Use syntax highlighting in code blocks with appropriate language tags.
- Employ tables for comparing options or features.
- Use diagrams (such as Mermaid) for explaining architecture or complex workflows.
- Consider light/dark mode compatibility for images.

## Examples

### Pythonic Pseudocode Example

```python
def query_builder(table_name, conditions=None, fields=None, order_by=None, limit=None):
    """Builds SQL queries with a chainable API.
    
    This is an example of the core functionality that would be described
    in a GitHub README for a query builder library.
    """
    # Default to selecting all fields if none specified
    selected_fields = "*"
    if fields and len(fields) > 0:
        selected_fields = ", ".join(fields)
    
    # Start building the base query
    query = f"SELECT {selected_fields} FROM {table_name}"
    
    # Add WHERE conditions if provided
    if conditions and len(conditions) > 0:
        where_clauses = []
        params = []
        
        for field, operator, value in conditions:
            where_clauses.append(f"{field} {operator} ?")
            params.append(value)
        
        query += " WHERE " + " AND ".join(where_clauses)
    
    # Add ORDER BY if specified
    if order_by:
        field, direction = order_by
        query += f" ORDER BY {field} {direction}"
    
    # Add LIMIT if specified
    if limit and limit > 0:
        query += f" LIMIT {limit}"
    
    return query, params

# Example usage - showing how the API would work
def example_usage():
    # Build a query to find active users, showing the chainable approach
    query, params = query_builder(
        table_name="users",
        fields=["id", "name", "email"],
        conditions=[("status", "=", "active"), ("last_login", ">", "2023-01-01")],
        order_by=("created_at", "DESC"),
        limit=10
    )
    
    # This would produce:
    # SELECT id, name, email FROM users WHERE status = ? AND last_login > ? ORDER BY created_at DESC LIMIT 10
    # params: ["active", "2023-01-01"]
    
    return query, params
```

### Preferred README Format:
```markdown
# Query Builder

A lightweight SQL query builder for Node.js that helps you construct complex database queries with a chainable API.

[![npm version](https://badge.fury.io/js/query-builder.svg)](https://badge.fury.io/js/query-builder)
[![Build Status](https://travis-ci.org/username/query-builder.svg?branch=main)](https://travis-ci.org/username/query-builder)
[![Coverage Status](https://coveralls.io/repos/github/username/query-builder/badge.svg?branch=main)](https://coveralls.io/github/username/query-builder?branch=main)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Installation

```bash
npm install query-builder --save
```

## Quick Start

```javascript
const { createQuery } = require('query-builder');

const query = createQuery()
  .select('users.id', 'users.name', 'profiles.avatar')
  .from('users')
  .join('profiles', 'users.id', 'profiles.user_id')
  .where('users.status', '=', 'active')
  .orderBy('users.created_at', 'desc')
  .limit(10);

const { sql, parameters } = query.toSQL();
// sql: SELECT users.id, users.name, profiles.avatar FROM users JOIN profiles ON users.id = profiles.user_id WHERE users.status = ? ORDER BY users.created_at DESC LIMIT 10
// parameters: ['active']
```

The query builder acts like a pipeline for your database operations. Much like water flowing through connected pipes, your data request flows through a chain of query components until it produces the exact SQL you need.

## Features

Our performance testing shows Query Builder processes complex joins 37% faster than similar libraries, while using 28% less memory.

- Type-safe query building with TypeScript support
- Protection against SQL injection
- Support for complex joins, subqueries, and unions
- Transaction support
- Compatible with multiple database engines
- Zero dependencies

## Documentation

Visit our [comprehensive documentation](https://query-builder.docs.com) for detailed API references and examples.

## Contributing

Contributions are welcome! Please read our [contributing guidelines](CONTRIBUTING.md) first.

## License

MIT
```

### Avoid:
```markdown
# QUERY BUILDER!!!

The ABSOLUTE BEST, EASIEST and most REVOLUTIONARY way to build SQL queries in Node.js!!!

## Super Easy Installation

Just do a simple npm install and you're ready to ROCK!

```bash
npm install query-builder
```

## Usage

Using our amazing library is INCREDIBLY SIMPLE!!! Look at this AWESOME example:

```javascript
// This code is SO EASY even a beginner could understand it!
const qb = require('query-builder');
const q = qb.new();
q.select('*').from('users').where('status', 'active');
const result = q.exec(); // BOOM! You're done!
```

Obviously, there's a TON more you can do with our GAME-CHANGING library, but this should get you started!

## Why We're The Best

- WAY FASTER than any other library
- UNBELIEVABLY EASY to use
- Will make your code INSANELY CLEAN
- Developed by INDUSTRY EXPERTS

Don't waste your time with inferior alternatives! Try Query Builder NOW and see the difference!!!
```
