<h1 align="center">AxonExplorer</h1>
<p align="center">Axon Explorer was fork on blockscout explorer project.</p>

## About
Axon Explorer was a explorer for [Axon](https://github.com/nervosnetwork/axon) Side Chain which is a layer2 network build on [Nervos Network](https://www.nervos.org/) [CKB](https://github.com/nervosnetwork/ckb)
## Getting Started
  1. install latest docker and docker compose
  2. run pg database on the host machine
  3. edit `xxx.env` file
  4. build command `docker-compose --env-file ./axon_staging.env -f ./docker-compose.yml build axon_explorer`
  5. run command `docker-compose --env-file ./axon_staging.env  -f ./docker-compose.yml up --force-recreate axon_explorer`
  6. use your env file instead of axon_staging.env
## Github Action
  1. setting your forked project environment: "axon_staging" (you can change it in your github workflow file)
  2. setting secret environment `ENV_FILE_PATH` which directing real path of your .env file on the deployment server
  3. pushing to `main` or `develop` branch (you can change it in your github workflow file)
  4. [`.env` fields meaning](./docs/envs_means.md)
  5. primary enviroment setting:  
    * ETHEREUM_JSONRPC_HTTP_URL (setting your chain node rpc endpoint)  
    * ETHEREUM_JSONRPC_TRACE_URL (setting your chain node rpc endpoint)  
    * DATABASE_URL (setting explorer access database url)  

## Acknowledgements
- We would like to thank the [Nervos Network](https://www.nervos.org/) for their funding support.  
- And also thanks to [blockscout](https://github.com/blockscout/blockscout) team, this project was forked from blockscout.

## Contributing
just fork and pull request

## License
[![License: GPL v3.0](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

This project is licensed under the GNU General Public License v3.0. See the [LICENSE](LICENSE) file for details.
