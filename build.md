BUILD image:


npm run tsc
cp package.json, .env and all non-js files into dist folder (because npm run tsc only transpiles ts into js)
cd dist

docker buildx build -t backend:slim .

PUSH image to repo:
docker login

docker tag d7f73e192c72c2955268432f2516e7ef22aefed2640a716ab5c5ee803b07cb86 snghbeer/nivon:backend

docker push snghbeer/nivon:backend

"docker run -p 8001:80 stripe_checkout:local"