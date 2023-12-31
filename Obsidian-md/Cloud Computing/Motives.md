### Ground Truth
Cloud Computing plays the core role in the development of the Android application to function, fully responsible for the APIs development. The APIs handle Android application requests to respond to a JSON format of information required by the app. The APIs that Cloud Computing is accountable for incorporate:
1. API 1
   - Version a: handling requests for nearby SOS stations
   - Version b: handling requests for user authentication
2. API 2: handling requests for transcribing a voice into text
3. API 3: handling requests for exercising face identification model
### Technique
1. We use JavaScript as our main and only programming language for Backend, followed by Node.JS as the runtime and Hapi.JS as the web framework. 
2. We use Cloud Run as our main and only computing service to handle requests and restrict the Cloud Run access (only the corresponding Cloud Run Invoker service account holder can invoke the service).
3. We use Cloud Firestore as our main database service to store users' identities, emails, and passwords. All data stored is encrypted.
4. We use Cloud Storage to store our Machine Learning model and to store users' faces with fine-grained access, granting users' privacy integrity.
5. We use Google Maps Platform as our main external API to develop API 1a.