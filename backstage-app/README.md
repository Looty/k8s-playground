# Creating Backstage Image
## Installing NVM
1. `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash`
2. restart terminal

## Installing npx
`npm install -g npx`

## Installing yarn
`npm install --global yarn`

## Building Backstage Image
1. `npx @backstage/create-app`
2. cd to folder
3. `yarn install --frozen-lockfile`
4. `yarn tsc`
5. `yarn build`
6. `docker image build . -f packages/backend/Dockerfile --tag backstage`

# Running Backstage
`docker run -p 7007:7007 backstage`