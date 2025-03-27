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

## Emotional Tone
- Project enthusiasm for the project without marketing hyperbole.
- Maintain a helpful, community-oriented voice.
- Be confident about project capabilities without overpromising.
- Acknowledge limitations or work-in-progress areas honestly.
- Focus on problem-solving rather than self-promotion.
- Express gratitude for contributions and community involvement.

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

## Phrases to Use
- "This project helps you..."
- "To get started:"
- "Here's a simple example:"
- "You might find it useful when..."
- "Contributions are welcome"
- "For more details, see the [documentation]"

## Phrases to Avoid
- "Best-in-class" or "industry-leading" (marketing language)
- "Simply" or "just" (minimizes complexity)
- "Easy to use" (subjective judgment)
- "Obviously" or "clearly" (presumptuous)
- "Revolutionary" or "game-changing" (hyperbolic)
- Excessive exclamation marks or all-caps emphasis

## Visual Elements
- Use descriptive alt text for all images and screenshots.
- Include animated GIFs for demonstrating workflows where helpful.
- Use syntax highlighting in code blocks with appropriate language tags.
- Employ tables for comparing options or features.
- Use diagrams for explaining architecture or complex workflows.
- Consider light/dark mode compatibility for images.

## Examples
### Preferred:
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

## Features

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
