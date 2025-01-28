import * as crypto from 'crypto';

// Generate a random string
const randomString = crypto.randomBytes(32).toString('hex');

// Hash the string
const hashedString = crypto.createHash('sha256').update(randomString).digest('hex');

// Encode the hashed string
const encodedString = Buffer.from(hashedString).toString('base64');

console.log(encodedString);
