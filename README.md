### Updating Everything:
Update all libraries with `apt update`, and then upgrade with `apt upgrade`.

### Installing Git:
Install git with `apt install git`.

### Installing Docker:
Install docker with `apt install docker.io`, and refer to the steps below to install docker-compose.

### Installing Docker Compose:
First, we're going to download the latest release of docker-compose:
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

Then, we'll need to apply executable permissions:
```
sudo chmod +x /usr/local/bin/docker-compose
```

Lastly, we need to remove the old link, and apply the new link:
```
$ sudo rm /usr/bin/docker-compose
$ sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```

### Downloading & Running Supabase:
Firstly, we need to download the Supabase files:
```
git clone --depth 1 https://github.com/supabase/supabase
```

Then, we'll go into the docker folder with everything saved:
```
cd supabase/docker
```

We'll copy the the example .env file:
```
cp .env.example .env
```

Lastly we'll start our Supabase instance!:
```
docker-compose up
```

Now, you should be able to visit your self-hosted Supabase instance on `ip:3000`!
