## Learn about PolyBlocks

### OVERALL SCHEME

#### ARTWORK

PolyBlocks allows anyone to create works of art freely. Up to 10000 tokens can be minted from each artwork.  
Once an artwork is minted, it is posted on PolyBlocks where collectors can mint (purchase) tokens from it.

#### TOKENS

Once a collector purchases one token from an artwork, an NFT (ERC-721 token) is minted.  
The tokens are also exchangeable on other NFT marketplaces such as OpenSea!

![scheme](img/guide.png?raw=true "scheme")

<br />

### STEP 1. Select an external library

PolyBlocks allows artists to use one external library at most. p5.js, threejs and SVG.js are currently available.  
If you prefer full scratch, you can of course choose no dependencies.  

<br />

### STEP 2. Write some JavaScript

There are several rules as follows:

- You need to choose a hash which will be used when your artwork appears on PolyBlocks. Please take a good hash to make your work more attractive!
- A different hash will be given to each token of that artwork, with which all the tokens can be differentiated.
- The hash can be accessed with the *pb.hash* variable.
- Use sfc32-based ***pb.random()* instead of *Math.random()* to feed a randomness** determined by the hash given to each token.
- The script should be **less than 50kb** otherwise you cannot store it on chain.
- See a full html template <a className="inline-anchor" href="https://polyblocks.io/learn/template">here</a> for your creation!

#### RANDOMNESS

We embed a JavaScript object called “pb”.

- “pb.hash” to get a unique hash value.
- “pb.random()” to get random values (0 to 1) determined by the hash.
- “pb.randrange(a, b)” to get a random number between two values determined by the hash. (a < r < b)
- “pb.randint(a, b)” to get a random integer between two values (a <= r <= b) determined by the hash.

PolyBlocks strongly recommends that all artists use “pb.random()”, "pb.randrange(a, b)" or "pb.randint(a, b)" to feed all of their project&apos;s randomness. It&apos;s a sft32-based algorithm generating values ranging between 0 and 1.
All the attributes of your piece should be derived from that hash so that users will be able to render the piece on their token and get the same results each time.

<br />

### STEP 3. Capture a thumbnail

Select a time before the capture is taken. This is useful to capture the best moment if your artwork is an ever-changing piece.

<br />

### STEP 4. Write metadata

This is the last step! You can fill in metadata such as the title, description, and price of the tokens.
