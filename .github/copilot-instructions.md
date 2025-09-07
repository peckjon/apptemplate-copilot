## Operator Interaction
- When asked to fix code, first explain the problems found.
- When asked to generate tests, first explain what tests will be created.
- When making multiple changes, provide a step-by-step overview first.

## Security
- Check the code for vulnerabilities after generating.
- Avoid hardcoding sensitive information like credentials or API keys.
- Use secure coding practices and validate all inputs.

## Environment Variables
- If a .env file exists, use it for local environment variables
- Document any new environment variables in README.md
- Provide example values in .env.example

## Version Control
- Keep commits atomic and focused on single changes
- Follow conventional commit message format
- Update .gitignore for new build artifacts or dependencies

## Code Style
- Follow existing project code style and conventions
- Add type hints and docstrings for all new functions
- Include comments for complex logic

## Change Logging
- Each time you generate code, note the changes in changelog.md
- Follow semantic versioning guidelines
- Include date and description of changes

## Testing Requirements
- Include unit tests for new functionality
- Maintain minimum 80% code coverage
- Add integration tests for API endpoints

## For Python Projects Only
- Always use a Python3 virtual environment: if no venv exists, create one and activate
- Always use and update a requirements.txt file for Python modules
- Follow PEP 8 style guidelines
- Include type hints (PEP 484)

## Flask + jQuery Integration
- Use jQuery for client-side interactivity with Flask/Jinja2 templates
- Include jQuery via CDN or download locally to `static/js/` directory
- Use `$(document).ready()` to ensure DOM is loaded before executing jQuery code
- Handle AJAX requests with jQuery's `$.ajax()`, `$.get()`, or `$.post()` methods
- Use Flask's `url_for()` function in templates to generate API endpoints for AJAX calls
- Implement proper error handling for AJAX requests with `.fail()` callbacks
- Use jQuery selectors and DOM manipulation methods for dynamic content updates
- Remember to copy updated JavaScript files to `static/js/` directory after changes
- **Template Configuration**: When using organized directory structure (app/templates/, app/static/), configure Flask app with explicit paths:
  ```python
  app = Flask(__name__, template_folder='app/templates', static_folder='app/static')
  ```
- **Template Path Issues**: If encountering `jinja2.exceptions.TemplateNotFound`, verify Flask is configured with correct template_folder path
- **Static Assets**: Ensure static files (CSS, JS, images) are properly configured and accessible via Flask's static_folder setting
