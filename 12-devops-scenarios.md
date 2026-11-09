Developer pushes code
        ↓
       Git
        ↓
GitHub webhook
        ↓
      Jenkins
        ↓
      Build
        ↓
      Test
        ↓
Docker image
        ↓
Deployment

Interview questions
How does Jenkins know that code was pushed?
Through a webhook or SCM polling, depending on the configuration. A GitHub webhook can notify Jenkins when a push occurs, triggering the pipeline.

Where does Jenkins get the source code?

Usually from Git:
git 'https://github.com/example/project.git'

or through the Jenkins Pipeline checkout/SCM configuration.