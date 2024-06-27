# esbuild-gas-plugin-issue-21

This repository is an error sample for https://github.com/mahaker/esbuild-gas-plugin/issues/21

## Error

Here is the result of `tsc --noEmit`.

```
  Types of property 'setup' are incompatible.
    Type '({ onEnd, initialOptions }: PluginBuild) => void' is not assignable to type '(build: PluginBuild) => void | Promise<void>'.
      Types of parameters '__0' and 'build' are incompatible.
        Type 'import("C:/Users/user/Documents/workspace/personal/esbuild-gas-plugin-issue-21/node_modules/.pnpm/esbuild@0.21.5/node_modules/esbuild/lib/main").PluginBuild' is not assignable to type 'import("C:/Users/user/Documents/workspace/personal/esbuild-gas-plugin-issue-21/node_modules/.pnpm/esbuild@0.18.20/node_modules/esbuild/lib/main").PluginBuild'.
          The types of 'initialOptions.plugins' are incompatible between these types.
            Type 'import("C:/Users/user/Documents/workspace/personal/esbuild-gas-plugin-issue-21/node_modules/.pnpm/esbuild@0.21.5/node_modules/esbuild/lib/main").Plugin[]' is not assignable to type 'import("C:/Users/user/Documents/workspace/personal/esbuild-gas-plugin-issue-21/node_modules/.pnpm/esbuild@0.18.20/node_modules/esbuild/lib/main").Plugin[]'.
              Type 'import("C:/Users/user/Documents/workspace/personal/esbuild-gas-plugin-issue-21/node_modules/.pnpm/esbuild@0.21.5/node_modules/esbuild/lib/main").Plugin' is not assignable to type 'import("C:/Users/user/Documents/workspace/personal/esbuild-gas-plugin-issue-21/node_modules/.pnpm/esbuild@0.18.20/node_modules/esbuild/lib/main").Plugin'.
                Types of property 'setup' are incompatible.
                  Type '(build: import("C:/Users/user/Documents/workspace/personal/esbuild-gas-plugin-issue-21/node_modules/.pnpm/esbuild@0.21.5/node_modules/esbuild/lib/main").PluginBuild) => void | Promise<...>' is not assignable to type '(build: import("C:/Users/user/Documents/workspace/personal/esbuild-gas-plugin-issue-21/node_modules/.pnpm/esbuild@0.18.20/node_modules/esbuild/lib/main").PluginBuild) => void | Promise<...>'.
                    Types of parameters 'build' and 'build' are incompatible.
                      Type 'import("C:/Users/user/Documents/workspace/personal/esbuild-gas-plugin-issue-21/node_modules/.pnpm/esbuild@0.18.20/node_modules/esbuild/lib/main").PluginBuild' is not assignable to type 'import("C:/Users/user/Documents/workspace/personal/esbuild-gas-plugin-issue-21/node_modules/.pnpm/esbuild@0.21.5/node_modules/esbuild/lib/main").PluginBuild'.
                        The types of 'initialOptions.tsconfigRaw' are incompatible between these types.
                          Type 'string | import("C:/Users/user/Documents/workspace/personal/esbuild-gas-plugin-issue-21/node_modules/.pnpm/esbuild@0.18.20/node_modules/esbuild/lib/main").TsconfigRaw' is not assignable to type 'string | import("C:/Users/user/Documents/workspace/personal/esbuild-gas-plugin-issue-21/node_modules/.pnpm/esbuild@0.21.5/node_modules/esbuild/lib/main").TsconfigRaw'.
                            Type 'TsconfigRaw' is not assignable to type 'string | TsconfigRaw'.
                              Type 'import("C:/Users/user/Documents/workspace/personal/esbuild-gas-plugin-issue-21/node_modules/.pnpm/esbuild@0.18.20/node_modules/esbuild/lib/main").TsconfigRaw' is not assignable to type 'import("C:/Users/user/Documents/workspace/personal/esbuild-gas-plugin-issue-21/node_modules/.pnpm/esbuild@0.21.5/node_modules/esbuild/lib/main").TsconfigRaw'.
                                The types of 'compilerOptions.baseUrl' are incompatible between these types.
                                  Type 'boolean' is not assignable to type 'string'.

8   plugins: [GasPlugin], // invalid
              ~~~~~~~~~


Found 1 error in esbuild.ts:8
```