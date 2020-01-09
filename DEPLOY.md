# Deployment

## General

The project is installed on the server in a way, so …

The following tools are necessary:
* ...
* ...

## Setup

The SSH-Key needs to be transfered to the server. In general use `ssh-copy-id` for this:
```bash
# example:
ssh-copy-id -i ~/.ssh/id_rsa.pub user@server
```

## Running the deployment

The following steps are necessary to run the deployment:

```bash
b5 deploy $SERVER $OPTIONS
```

`$SERVER` could be:
* staging
* production

`$OPTIONS` could be (separate multiple values by ","):
* nostatic
* nomigrate

The following steps are going to happen while deployment:
* ...
* Enabling maintenance mode
* Run migrations ...
* ...
* Disabling maintenance mode

### Example

```bash
b5 deploy staging nomigrate,nostatic
```

## Please check

After the deployment you should check the following:
* Frontpage is available and working: https://www.domain.com/
* ...

