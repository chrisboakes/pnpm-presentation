# Why you should probably use pnpm

- [Chris Boakes](https://chrisboakes.com/)
- Twitter: [@cboakes](https://twitter.com/cboakes)
- GitHub: [@chrisboakes](https://github.com/chrisboakes)

![Everyone hates node modules](/images/node-modules-wtf.jpg)

## What is pnpm?

A "fast, disk space efficient package manager"

## Why use pnpm?

- Up to 2x faster than other package managers
- Super efficient - `pnpm` writes only ONE unique file on a disk. `node_modules` are hard linked from a single content-addressable store instead of making copies
- If you have multiple projects using the same dependency it doesn't copy the shared dependency

## What is a hard link?

- Hard links point to the same place on the disk where the original files are
- If you have `foo` in your project as a dependency and it occupies 1MB of space, it will look like it occupies 1MB of space in the project's `node_modules` folder as well as the pnpm global store
- However, that 1MB is *the same space* on the disk addressed from two different locations. So in total `foo` occupies 1MB, not 2MB.

## Further installs

- Dependencies will link to the files that were already created by the first install

## Demo

Live demo

## Switching from npm to pnpm

- Delete `package-lock`. Run `pnpm i`
- Generates a `pnpm-lock`
- More on [https://pnpm.io/](https://pnpm.io/)

## Conclusion

- Speedy
- Super disk space efficient
- Easy to switch to

## Thanks

Slides and demo: 
