# Occam
![razor logo](./razor200.png)
[logo source](https://www.onlinewebfonts.com/icon/556013)

A proof-of-concept Web application based on the _Occam's razor_ problem-solving principle:
> With competing hypothetical answers to a problem, one should select the one that makes the fewest assumptions.

### Architecture
- Two-tier hemilith:
	- Backend: SQL, AWS Lambda
	- Frontend: Web Components

### Buzzwords
- Zero dependencies
- First principles

### Constraints
- Not importing any third-party code
- Not using any framework
- Using only vanilla JavaScript, HTML, and CSS
- All styles and logic should be encapsulated in the HTML; no application code should be exposed.

### Backend
- Contains ERP business logistics ("everything a company that buys and sells shit does")
- Converts HTTP request to database request
- Bypasses middleware (web server, etc.)
- Implements security on each Lambda via roles
- Each SQL request has to go through a Lambda before it reaches database
- Version control and collaboration:
	- source code is hosted within the Lambda
	- each time a Lambda is updated, it's a new version

### Frontend
- Web components
	- Single HTML page
	- `Date` widget
	- `Select facility` dropdown
- HTML files hosted on S3
	- `GET` goes to S3
	- `POST` goes to Lambda SQL
