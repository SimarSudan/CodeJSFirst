/*
Assessment Requirements
1. Create a variable that can hold a number of NFT's. What type of variable might this be?
2. Create an object inside your mintNFT function that will hold the metadata for your NFTs. 
   The metadata values will be passed to the function as parameters. When the NFT is ready, 
   you will store it in the variable you created in step 1
3. Your listNFTs() function will print all of your NFTs metadata to the console (i.e. console.log("Name: " + someNFT.name))
4. For good measure, getTotalSupply() should return the number of NFT's you have created
*/

// Step 1: Create a variable to hold your NFTs
let mintedNFTs = [];

// Step 2: Create an object inside your mintNFT function
// This function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function mintNFT(title, creator, yearCreated) {
  const nft = {
    title: title,
    creator: creator,
    yearCreated: yearCreated,
  };
  mintedNFTs.push(nft);
}

// Step 3: Create a "loop" that will go through an "array" of NFTs
// and print their metadata with console.log()
function listNFTs() {
  console.log("** Your Minted NFTs **");
  mintedNFTs.forEach(nft => {
    console.log("Title: " + nft.title);
    console.log("Creator: " + nft.creator);
    console.log("Year Created: " + nft.yearCreated);
    console.log("-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-");
  });
}

// Step 4: Print the total number of NFTs we have minted to the console
function getTotalSupply() {
  return mintedNFTs.length;
}

// Call your functions below this line

mintNFT("Abstract Art Piece", "Sam", 2023);
mintNFT("Digital Landscape", "Simar", 2022);

console.log("Total NFTs minted: " + getTotalSupply());
listNFTs();
