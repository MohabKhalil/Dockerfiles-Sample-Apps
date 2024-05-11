First stage ("builder"): This uses an Alpine image with Go installed to build Go application. It copies the source files into the image and compiles them.\
Second stage: This uses a plain Alpine Linux image (which is very small) and copies the compiled executable from the first stage. It then sets the command to run your application.
