## Hi there 👋

<!--
**mandeep-bit/mandeep-bit** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

// components/Header.js
import React from 'react';

const Header = () => {
  return (
    <header>
      <nav>
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">Profile</a></li>
          <li><a href="#">Explore</a></li>
        </ul>
      </nav>
    </header>
  );
};

export default Header;
// api/users.js
const express = require('express');
const router = express.Router();
const User = require('../models/User');

router.get('/', async (req, res) => {
  const users = await User.find().exec();
  res.json(users);
});

router.post('/', async (req, res) => {
  const user = new User(req.body);
  await user.save();
  res.json(user);
});

module.exports = router;
# connecto database
use connecto

# users collection
db.createCollection("users", {
  validator: {
    $jsonSchema: {
      bsonType: "object",
      required: ["name", "email", "password"],
      properties: {
        name: {
          bsonType: "string",
          description: "Name of the user"
        },
        email: {
          bsonType: "string",
          description: "Email address of the user"
        },
        password: {
          bsonType: "string",
          description: "Password of the user"
        }
      }
    }
  }
})
