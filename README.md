# Example Nx Fix Repository

### https://github.com/nrwl/nx/issues/22146#issue-2168133699

```

ERROR  failed to read input source map: failed to parse inline source map url
";


Caused by:
    relative URL without a base
    at C:\Users\runneradmin\.cargo\registry\src\index.crates.io-6f17d22bba15001f\swc-0.272.4\src\lib.rs:385


> nx run my-nest-app:echo

Executor ran for Echo { textToEcho: 'Hello World' }

```

The following error can be fixed simply by installing `nx-cloud` as a dependency

```
npm i nx-cloud
```

Run the `echo` target on the `apps/my-nest-app` to see the local executor run without issues

```
nx echo my-nest-app
```
