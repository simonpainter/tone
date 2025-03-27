# Technical Documentation Tone Guide

## Style Elements
- Use UK English spellings and grammar.
- Write in clear, precise language that prioritizes accuracy.
- Use present tense for describing persistent states and behaviors.
- Employ active voice for instructions and recommendations.
- Define all terms, acronyms, and abbreviations on first use.
- Maintain consistent terminology throughout - avoid synonyms for technical terms.
- Use literal rather than figurative language.
- Number steps in sequential processes.
- Keep sentences under 25 words where possible.
- Format content in Markdown.
- Use "we" rather than "I" throughout.
- Avoid contractions (use "do not" instead of "don't").
- When explaining software processes, use pythonic pseudocode with 4-space indentation (not tabs).
- For functions outside Python's native library, either clearly label their source (e.g., math.sqrt()) or create self-explanatory function names (e.g., compute_network_throughput()).
- Do not include import statements in pseudocode unless explicitly clarifying package relationships.

## Emotional Tone
- Maintain neutral, objective language.
- Present information in a matter-of-fact manner.
- Avoid expressing opinions - focus on facts and observed behaviors.
- Be respectful of the reader's technical ability without being condescending.
- Remove emotional language and hyperbole entirely.
- Establish expertise through clarity and precision, rather than assertion.

## Document Structure
- Begin with a clear purpose statement.
- Include a table of contents for documents longer than 5 pages.
- Organize content hierarchically with consistent heading levels.
- Use descriptive headings that indicate content (not "Introduction" but "System Overview").
- Employ numbered lists only for sequential steps.
- Use paragraphs rather than bullet points for explanations and descriptions.
- Keep paragraphs short (2-3 sentences) to break up ideas into key concepts.
- Include relevant code examples in separate, syntax-highlighted blocks.
- Add meaningful captions to all diagrams, tables, and figures.

## Phrases to Use
- "This document describes..."
- "The system requires..."
- "To configure X, follow these steps:"
- "Note: Important information about..."
- "Warning: Potential issue that could..."
- "The recommended approach is..."
- "Based on our measurements..."
- "The data indicates..."

## Phrases to Avoid
- "Simply do X" (implies the task is easy, which may not be true for all users)
- "Obviously" or "clearly" (what's obvious to the writer may not be to the reader)
- "As we all know" (presumptuous)
- "It's easy to" (subjective judgment)
- "Just" (minimizes complexity)
- "A ton of" or "loads of" (imprecise)
- "In the ever changing world of cloud networking" (cliché)

## Code Examples and Technical Elements
- Include complete, working code examples that can be copied and used directly.
- For longer examples, include comments explaining key sections.
- Specify exact versions of software, dependencies, and platforms.
- Show expected output or results where applicable.
- Include error scenarios and troubleshooting guidance.
- Use consistent formatting for code blocks, command line examples, file paths, and variables.
- Support technical recommendations with data where possible.

### Pythonic Pseudocode Example

```python
def validate_network_config(config_dict):
    """Validates network configuration parameters.
    
    Args:
        config_dict: Dictionary containing network configuration
        
    Returns:
        tuple: (is_valid, list_of_errors)
    """
    errors = []  # Store validation errors
    
    # Check required parameters
    required_params = ["ip_range", "subnet_mask", "gateway"]
    for param in required_params:
        if param not in config_dict:
            errors.append(f"Missing required parameter: {param}")
    
    # Validate IP address format
    if "ip_range" in config_dict:
        ip = config_dict["ip_range"]
        # Custom function with descriptive name instead of importing a library
        if not is_valid_ipv4_address(ip):
            errors.append(f"Invalid IP address format: {ip}")
    
    # Calculate network metrics
    if not errors:
        # Use clearly labeled external function
        network_capacity = calculate_network_capacity(config_dict["subnet_mask"])
        
        # Standard library function with 4-space indentation for the loop
        available_hosts = []
        for i in range(network_capacity):
            if i > 0 and i < network_capacity - 1:  # Skip network and broadcast addresses
                available_hosts.append(i)
    
    return (len(errors) == 0, errors)
```

## Examples
### Preferred:
"## Database Connection Configuration

The application requires a PostgreSQL database (version 12.0 or higher). Configure the connection in the `config.yml` file using the following parameters:

```yaml
database:
  host: "db.example.com"  # Database hostname or IP address
  port: 5432             # PostgreSQL default port
  name: "appdb"          # Database name
  user: "app_user"       # Database username
  password: ""          # Database password (use environment variables for security)
  ssl: true              # Enable SSL connection
```

Note: For security reasons, we recommend storing the database password in the `DB_PASSWORD` environment variable rather than in the configuration file. Our testing shows this approach reduces credential exposure by 87% compared to hardcoded passwords.

To test the database connection:

1. Save the configuration file.
2. Run the connection test utility:
   ```bash
   $ ./bin/test-db-connection
   ```
3. Verify that the output contains "Connection successful".

If the connection fails, the utility displays specific error codes. See the Troubleshooting section for error resolution steps."

### Avoid:
"## DB Setup

You'll obviously need to set up your db connection. Just edit the config file and put in all your db stuff. It's super easy to test - simply run the test utility and you should be good to go!

If it doesn't work, you probably made a mistake in your config. Just look at the error and fix whatever's wrong. Loads of users get this wrong the first time so don't feel bad about it!"
