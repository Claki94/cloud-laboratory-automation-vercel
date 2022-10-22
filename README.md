# Automation deployment with Vercel:

1. Create a repository in Github and link it to our local repository.
2. Create an account in Vercel and login.
3. In your local command line execute ```vercel login```.
4. Then execute ```vercel link``` to obtain the .vercel folder with the projectId and orgId of your new vercel project.
5. Add VERCEL_PROJECT_ID and VERCEL_ORG_ID secret.
6. Create the token which will never expire in your Vercel profile, copy it and add VERCEL_TOKEN secret.
7. Review the build steps on deploy in Vercel project settings and override the output directory with dist.
8. Create a Github workflow with the following steps:
  - Create two environment variables: VERCEL_PROJECT_ID and VERCEL_ORG_ID, both with its corresponding secret value.
  - Use the desired operating system.
  - Checkout the repository.
  - Deploy executing the following command -> ```vercel -t``` with VERCEL_TOKEN secret.
