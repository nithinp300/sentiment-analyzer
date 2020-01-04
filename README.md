# Sentiment Analyzer
This web application takes a sentence as input. Using text analysis, it calculates
the emotion of the sentence.

The application consists of three microservices:

frontend: A Nginx web server that serves the React.js static files.
webapp: A Spring/Java web application that handles requests from the frontend
logic: A Flask/Python application that performs the sentiment analysis.

The data flow between the microservices:
1. A client application requests the index.html. This in turn requests bundled
scripts of React application.
2. The user interacting with the React application triggers the requests to
the Spring web application.
3. The Spring web application forwards the requests to the Flask app to do
sentiment analysis.
4. Flask application calculates the sentiment and returns the result as a response.
5. The Spring web application returns the response to the React application.
