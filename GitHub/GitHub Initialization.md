# HOWTO initialize a repository on GitHub

1. Initialize a repository
``` Git
git init
```

2. Commit if you never did
``` Git
git add .
git commit -m "first commit"
```

3. Add path to GitHub repository
``` Git
git remote add origin _url_
```

4. Synchronize with GitHub repository
``` Git
git push -u origin main
```