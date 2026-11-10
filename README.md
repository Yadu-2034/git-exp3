#Create a Docker Hub repository
This experiment pushes a different Docker image, so create a new Docker Hub repository.
1. Open Docker Hub.
2. Click Create repository.
3. Repository name: python-ci-lab.
4. Visibility: Public.
5. Click Create.
7. Create a Docker Hub access token
#GitHub needs permission to upload your Docker image.
1. In Docker Hub, open Account Settings → Personal access tokens (or Security).
2. Click Generate new token.
3. Give it a name, such as github-actions.
4. Select read and write permissions.
5. Generate and copy the token.
#Keep the token private. Do not share it or put it directly in your YAML file.
8. Add GitHub Secrets
Open your GitHub repository:
1. Go to Settings.
2. Open Secrets and variables → Actions.
3. Click New repository secret.
Create these two secrets:
Secret name	Value
DOCKERHUB_USERNAME	Your Docker Hub username
DOCKERHUB_TOKEN	The access token you just generated

git init
git add .
git commit -m "init lab"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/python-ci-docker-lab.git
git push -u origin main
