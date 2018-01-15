# Webpack for connected Front Ends

## Run
Install dependencies:
```
npm i
```

run webpack:
```
npm run webpack
```
this will bundle what's in the entry file and its imports and output it in the /build directory.

Check out the changes by navigating to the index.html file, or start a server in the project's root directory with:
```
python -m SimpleHTTPServer 3001
```

## Reason
For a long time, I had the notion that webpack could only be ran for set ups that are independent from the back end. For example SPAs that only communicate with AJAX.

I closed my mind into thinking that it had to be ran with a development server. You would make the webpack config file and use that to run the dev server. That would do all the cool things like Hot Module Replacement and having all the JS in RAM so changes would be blazing fast. Then, when you needed to actually use it for production, you would do a build and be done with it.

I blame the tutorials and webpack docs partly, because when I started looking into webpack around 2 years ago  all the examples where like what I mentioned before, independent set ups.

But you can also use webpack to develop in a set up where you have the back end connected with the front, for example with a templating language. All you need to do is define an input file and output directory in your webpack config. Then you run ```webpack -w``` and that's it. It will watch for changes, and then do what it does, and throw it to the output directory you specified. After that, you just point to the output file in your template like ```<script src="./build/index.js" />```. This project does just that, as simple as possible.

You won't benefit from HMR, but at least you CAN use webpack for these connected set ups which are much more common in the professional world.

Webpack can be simple too.
