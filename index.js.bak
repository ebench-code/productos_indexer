require('dotenv').config();
const algoliasearch = require('algoliasearch');
//define API parms from app environment
const algoliaAppId = process.env.Productos_App_Id;
const algoliaAdminKey = process.env.Productos_Admin_Key;
const client = algoliasearch(algoliaAppId,algoliaAdminKey);
// Obtain data from source
const productos = require("./algolia payload.json");
// send data to the index
const index = client.initIndex('products-import');
index.replaceAllObjects(productos);
// Code to connect to MongoDb directly
//const mongoose = require('mongoose');

// Replace 'localhost' with the IP address of your MongoDB server if it's not running locally.
// Use the correct port if your MongoDB server is not running on the default port (27017).
const mongoURI = 'mongodb://localhost:27017/products';

//mongoose.connect(mongoURI, { useNewUrlParser: true, useUnifiedTopology: true });

//const db = mongoose.connection;

//db.on('error', (error) => {
//  console.error('Connection error:', error);
//});

//db.once('open', () => {
//  console.log('Connected to the database.');
//});

// Example to select product index details:

// Define a schema for the "products_index" collection
//const productSchema = new mongoose.Schema({
 //   name: String,
 //   price: Number,
// });
  
  // Create a model based on the schema
//  const Product = mongoose.model('Product', productSchema, 'products_index');
  
  // Fetch all documents from the "products_index" collection
//  Product.find({}, (err, products) => {
 //   if (err) {
 //     console.error('Error fetching products:', err);
 //     return;
 //   }
  
 //   console.log('Products found:', products);
    // Close the database connection when you're done with it
 //   db.close();
 // });






