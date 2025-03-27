# User Guide/Tutorial Tone Guide

## Style Elements
- Use UK English spellings and grammar.
- Write in clear, straightforward language accessible to non-experts.
- Use second-person pronouns ("you") to address the reader directly.
- Keep sentences short and focused on one idea.
- Use active voice for instructions.
- Avoid technical jargon unless absolutely necessary (and define it when used).
- Maintain consistent terminology throughout.
- Use shorter paragraphs (2-3 sentences maximum).
- Format content in Markdown.
- Use "we" rather than "I" when referring to the guide's creators.
- Use contractions sparingly, and only in more conversational sections.
- When explaining software processes, use pythonic pseudocode with 4-space indentation (not tabs).
- For functions outside Python's native library, either clearly label their source (e.g., math.sqrt()) or create self-explanatory function names (e.g., check_connection_status()).
- Ensure pseudocode is beginner-friendly with clear comments explaining purpose and steps.

## Emotional Tone
- Be encouraging and supportive without being patronizing.
- Project confidence that the reader can succeed.
- Acknowledge potential frustration points with empathy.
- Use a conversational but professional tone.
- Be patient with repetition of core concepts.
- Avoid humor that might not translate across cultures.
- Use analogies and metaphors to explain complex technical concepts.

## Document Structure
- Begin with clear learning objectives or outcomes.
- Present a logical progression from basic to advanced concepts.
- Include a "What You'll Need" section upfront.
- Break content into digestible sections with descriptive headings.
- Use numbered steps for sequential tasks.
- Include visual aids (screenshots, diagrams) for complex steps.
- Provide "Try It Yourself" exercises to reinforce learning.
- End each major section with a brief summary.
- Include troubleshooting sections for common issues.
- Use paragraphs rather than bullet points for explanations.

## Phrases to Use
- "In this section, you'll learn how to..."
- "First, let's understand what X does..."
- "Try this yourself:"
- "You might notice that..."
- "If X doesn't work as expected, check that..."
- "Let's break this down step by step:"
- "Here's an example to illustrate how this works:"
- "Our testing shows..."

## Phrases to Avoid
- "Simply" or "just" (minimizes complexity)
- "Obviously" or "clearly" (can make users feel inadequate)
- "As we discussed earlier" (user may be reading out of order)
- "It's easy to" (subjective judgment)
- "All users should know" (presumes knowledge)
- "Always" or "never" (often inaccurate absolutes)
- "In the ever changing world of cloud networking" (cliché)

## Visual Elements
- Use annotated screenshots to highlight important UI elements.
- Include "before and after" images when applicable.
- Use consistent visual indicators (arrows, highlights, boxes).
- Number visual elements that correspond to numbered steps.
- Include alt text for accessibility.
- Use diagrams (such as Mermaid) for conceptual explanations.
- Include data visualizations when explaining performance considerations.

## Examples
### Preferred:
"## Configuring Your First Network Security Group

In this section, you'll learn how to create and configure a network security group to protect your cloud resources.

### What You'll Need
- An active cloud account with administrator access
- About 10 minutes
- Your network IP range information

### Understanding Network Security Groups

A network security group works like a virtual firewall for your cloud resources. Think of it as a security guard that checks ID cards before letting visitors into a building. The guard uses a ruleset to determine who can enter and what areas they can access.

Our testing shows properly configured security groups can block over 90% of common network-based attacks.

#### How Security Groups Work (Pseudocode Example):

```python
def apply_security_rules(incoming_traffic, security_group):
    """Evaluates incoming network traffic against security group rules.
    
    This function checks if traffic should be allowed through based on
    security group settings - just like how a security guard checks IDs.
    """
    # Start with a default deny policy
    access_granted = False
    reason = "Default deny - no matching rules"
    
    # Check each incoming connection against our rules
    for rule in security_group.rules:
        # Check if this traffic matches the rule's criteria
        if matches_rule_criteria(incoming_traffic, rule):  # Clear, descriptive function name
            if rule.action == "ALLOW":
                access_granted = True
                reason = f"Allowed by rule: {rule.name}"
                break  # Stop checking once we find a match
            elif rule.action == "DENY":
                access_granted = False
                reason = f"Explicitly denied by rule: {rule.name}"
                break
    
    # Log the decision for security auditing
    log_security_event(incoming_traffic, access_granted, reason)
    
    return access_granted
```

### Steps

1. Log in to your cloud dashboard at cloud.example.com

2. Navigate to Security > Network Security Groups.
   ![Security menu with Network Security Groups option highlighted](/images/security-menu.png)

3. Click "Create New Group".
   
   The system automatically suggests a name based on your account structure. You can change this if you prefer a different naming convention.

4. Define your network boundaries by entering your IP range in CIDR notation (e.g., 10.0.0.0/24).

5. Set up your first inbound rule by defining:
   - Protocol: TCP
   - Port Range: 443
   - Source: Your office IP address
   
   This creates a secure HTTPS connection pathway while blocking other access attempts.

Your new security group is now active and protecting the defined network segment. The dashboard shows the protection status in real-time.

### Troubleshooting

If you can't access resources after creating the security group:

Check that your current IP address matches the one you authorized. IP addresses can change if you're using dynamic addressing.

Verify that the correct protocols and ports are open for your application's requirements. For example, a web server typically needs port 80 (HTTP) and 443 (HTTPS) open.

Review the security group logs for blocked connection attempts, which might indicate you need to adjust your rules.

### Try It Yourself
Create a second security group that allows SSH access (port 22) only from your current IP address. Then attach it to a test server and verify you can connect."

### Avoid:
"## Security Groups

Setting up security groups is super easy! Just click around until you find the security section and then add some rules. It's really simple and you'll have your security configured in no time!

Obviously you need to be logged in first. Then just find the security section (it's clearly visible in the menu) and click it. Then you simply create a new group - make sure it's a good one! Then just set up some rules (whatever you need!) and hit the button. Boom! You're done!

If it doesn't work you probably did something wrong. Check everything and try again. It's really not complicated at all, so you should get it working without any issues."
