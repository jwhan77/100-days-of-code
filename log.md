# 100 Days Of Code - Log

### Day 1: Oct 20, 2021

**Today's Progress**: Added GitHub provider in Next.js project with next-auth

**Thoughts** I don't think I understand how it works yet. Need to study more.

**Link(s) to work**
[link](https://github.com/jwhan77/next-tailwind-test/commit/6395b9875575092af3364a8c423c9b8317034d84)

### Day 2: Oct 21, 2021

**Today's Progress**: Learned how to use NextAuth GitHub provider access token into Octokit for using GitHub's REST APIs.

**Thoughts**: I kept trying to use CSRF token for Octokit auth. And I realized Octokit require github access token. It happened because I didn't fully understand what CSRF token is.

**Link(s) to work**
[link](https://github.com/jwhan77/next-tailwind-test/commit/11b19dae05d5fe086d3991c6962e15aa708d7644)

### Day 3: Oct 22, 2021

**Today's Progress**: Added grid and tooltip

**Thoughts**: Tried to figure out why all 100 tooltips showed up at the same time.

**Link(s) to work**
[grid](https://github.com/jwhan77/next-tailwind-test/commit/5b128b5777adfa63f71f54dc7759c213feb3a9d8)
[tooltip](https://github.com/jwhan77/next-tailwind-test/commit/691631d1054fadae8c909700d7c21490f064dafd)

### Day 4: Oct 23, 2021

**Today's Progress**: Show user's repositories, including private.

**Thoughts**: `GET /user/repos` was supposed to list authenticated user's repositories including private but it didn't. I assumed it was because of using GitHub App client ID and Secret in provider. So I use OAuth App's and now it works.

**Link(s) to work**
[link](https://github.com/jwhan77/next-tailwind-test/commit/747a62397df3787de7ab7db5c7da04603b4c5e31)

### Day 5: Oct 24, 2021

**Today's Progress**: Learned how to integrate MongoDB into the Next.js App.

**Thoughts**: I'm still trying to figure out how to use MongoDB Adapter in the NextAuth provider since NextAuth v3 docs for that don't exist.

**Link(s) to work**
[link](https://github.com/jwhan77/next-mongodb-test)

### Day 6: Oct 26, 2021

**Today's Progress**: Add MongoDB adapter

**Thoughts**: I added MongoDB adapter using TypeORM adapter. 

**Link(s) to work**
[link](https://github.com/jwhan77/next-tailwind-test/commit/65b29809d183411ea47bb899bbf1ecbd0d301305)

### Day 7: Oct 27, 2021

**Today's Progress**: Fixed GitHub access token issue that happened after adding MongoDB adapter.

**Thoughts**: JWT callback doesn't work after adding the database adapter. I fixed it by updating GitHub access token every time the user login. 

**Link(s) to work**
[link](https://github.com/jwhan77/next-tailwind-test/commit/0d00bf9372285df0839a7edef99af2a823101ce1)

### Day 8: Oct 28, 2021

**Today's Progress**: Changed Schema type

**Thoughts**: Everytime I make changes, it gives me new errors. I think I need to change User model code.

**Link(s) to work**
[link](https://github.com/jwhan77/next-tailwind-test/commit/aa22e3c015952efe2fdf9c3cbb72299ca0210416)

### Day 9: Oct 29, 2021

**Today's Progress**: I tried to fix User model issue, but no progress.

**Thoughts**: With the NextAuth.js v3 TypeORM approach, I can't access to User model after connecting to db, which I can't use .find() functions, because mongoose.model("User", User) doesn't work. So I changed User.js like the other model with using mongoose.Schema. And now it has error in adapter in [...nextauth].js. It makes no sense. I expected Adapters.TypeORM.Models.User.schema returns Schema but it doesn't. I have no idea how to use .find() with User model omg.

**Link(s) to work**
no link