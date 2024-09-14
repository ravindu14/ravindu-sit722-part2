1. Build a docker image for this project.

   - docker build -t book_catalog .

2. Verify image by running image locally. Pass Render

   - docker run -d -p 8000:8000 -e DATABASE_URL=<'Database URL'> book_catalog

3. Access the application in browser.

   - http://localhost:8080/docs

4. Deploy the app into kubernetes cluster.

   - kubectl apply -f scripts/deployment.yml

5. Verify the status of kubernetes instance using following commands.

   - kubectl get pods
   - kubectl get deployments
   - kubectl get services

6. Access the application using externalIP output from kubectl services. As the application using default port 80, just access localhost.
   - http://localhost/docs
