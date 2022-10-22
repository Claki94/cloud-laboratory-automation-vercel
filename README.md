# Automation deployment with Github pages:

1. Create a repository in Github and link it to our local repository.
2. Create a public/private key pair for the project.
3. Upload the private key to the project's Secrets.
4. Upload the public key to the project's Deploy keys.
5. Create a Github workflow with the following steps:

- Use the desired operating system.
- Checkout the repository.
- Create an .ssh folder in the working directory to copy the SSH private key from the Secrets.
- Configure Git with an email and username.
- Install project dependencies.
- Build the project for production.
- Run the deploy command which internally uses the gh-pages command to do automated deploy.
