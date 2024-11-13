# pnpm install – use-node-version bug

## to reproduce

1. Clone this repo
2. Run `pnpm env use 20 -g` to enable node 20'
3. Run `node -v` to verify that node 20 is enabled
3. Run `pnpm test-version v22.0.0` to see that the script gets run with node 22
4. Run `node -v` to see that node 20 is still enabled
5. Run `pnpm install` to see that install uses the global v20 and not the v22 it should