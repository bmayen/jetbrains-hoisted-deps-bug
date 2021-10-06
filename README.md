# jetbrains-hoisted-deps-bug

## Steps to recreate

1. Using NPM v7, run `npm i` from the monorepo root folder
2. In Webstorm, open `client/lib/projects/project2/index.ts` and see that autocomplete works in the import statement defined at the top. 
3. Now open `client/lib/projects/project1/index.ts` and see that autocomplete does not work in the import statement defined at the top. 

Project2 has unique dependencies that do not get hoisted and autocomplete works with the node_modules located within that folder. Project1 has dependencies that do get hoisted and autocomplete does not work with the node_modules at the monorepo root.
