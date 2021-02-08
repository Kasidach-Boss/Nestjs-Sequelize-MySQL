<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo_text.svg" width="320" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">A progressive <a href="http://nodejs.org" target="_blank">Node.js</a> framework for building efficient and scalable server-side applications.</p>
    <p align="center">
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/dm/@nestjs/common.svg" alt="NPM Downloads" /></a>
<a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
<a href="https://coveralls.io/github/nestjs/nest?branch=master" target="_blank"><img src="https://coveralls.io/repos/github/nestjs/nest/badge.svg?branch=master#9" alt="Coverage" /></a>
<a href="https://discord.gg/G7Qnnhy" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
<a href="https://opencollective.com/nest#backer" target="_blank"><img src="https://opencollective.com/nest/backers/badge.svg" alt="Backers on Open Collective" /></a>
<a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://opencollective.com/nest/sponsors/badge.svg" alt="Sponsors on Open Collective" /></a>
  <a href="https://paypal.me/kamilmysliwiec" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-ff3f59.svg"/></a>
    <a href="https://opencollective.com/nest#sponsor"  target="_blank"><img src="https://img.shields.io/badge/Support%20us-Open%20Collective-41B883.svg" alt="Support us"></a>
  <a href="https://twitter.com/nestframework" target="_blank"><img src="https://img.shields.io/twitter/follow/nestframework.svg?style=social&label=Follow"></a>
</p>
  <!--[![Backers on Open Collective](https://opencollective.com/nest/backers/badge.svg)](https://opencollective.com/nest#backer)
  [![Sponsors on Open Collective](https://opencollective.com/nest/sponsors/badge.svg)](https://opencollective.com/nest#sponsor)-->

## Description

[Nest](https://github.com/nestjs/nest) framework TypeScript starter repository.

## Installation

```bash
$ npm install
```

## Running the app

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```
## ไกด์ให้
```
1. ตัวที่ต้องติดตั้ง MySQL ให้ไปที่ https://dev.mysql.com/downloads/workbench/
2. ก่อนรัน วิธีที่ง่ายที่สุดให้เปิด Xampp และ start ที่ MySQL ไม่งั้นมันจะขึ้น Error ไม่สามารถเชื่อมกับ database ได้ แต่จะใช้ docker ก็ทำได้แต่ยากกว่า (port ที่ mysql ทำงาน คือ 3306)
3. password แนะนำให้ปล่อยว่างไว้ เช่น password: ''
4. สามารถทดสอบการ get post ซึ่งเป็นการจัดการหลังบ้าน ทำได้โดยใช้โปรแกรม Postman ไปโหลดได้ที่ https://www.postman.com/downloads/
5.การทำงานของ Nestjs คือ หลักๆจะต้องเขียน service ขึ้นมา และตัว conttroller จะทำหน้าที่เรียก service มาใช้ ซึ่งสั่งว่า get ให้ทำอะไร หรือ post ทำอะไร 
  - ส่วนตัว module ก็จะเกิดจาก service, controller และ class ของ entity มาประกอบกัน
  - ส่วน entity คือ โครงสร้างของตารางว่าเราจะให้มีอะไร
@Post()
    create(@Body() createUserDto:CreateUserDto): Promise<User> {
        return this.usersService.create(createUserDto);
    }
    อธิบาย: มันจะเป็นการที่ใช้ไฟล์ create-user.dto.ts มาสร้างเป็น User ที่เก็บเนี่ย 1 คน ซึ่งจะตาม user.model.ts ใน file (Promise เป็นการเรียก class User)
    ส่วนฟังก์ชันต่างๆ เช่น
    findall() คือ แสดงข้อมูลทั้งหมด
    findone() คือ แสดงแค่คนเดียว
    remove() คือ ลบ user
    
```
## ใช้ Postman
```
  การใช้ postman เราจะใช้ localhost:3000 เพราะ await app.listen(3000); ใน main.ts จะใช้ port อื่นก็ได้ตามใจเลย
  การ Post เราก็ใช้ localhost:3000/users
  การ Get เราก็ใช้ localhost:3000/users/{id} เช่น localhost:3000/users/1

```
## Test

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```
## ติดตั้ง Package

```bash
# กรณี Error ที่ rxjs ให้ติดตั้งตัวนี้
$ npm i rxjs

# ติดตั้งpakage sequelize typescript 
$ npm install --save sequelize sequelize-typescript mysql2
$ npm install --save-dev @types/sequelize
# ถ้า Error ที่ @nestjs/sequelize ให้ติดตั้งตัวนี้
$ npm i @nestjs/sequelize

```

## Support

Nest is an MIT-licensed open source project. It can grow thanks to the sponsors and support by the amazing backers. If you'd like to join them, please [read more here](https://docs.nestjs.com/support).

## Stay in touch

- Author - [Kamil Myśliwiec](https://kamilmysliwiec.com)
- Website - [https://nestjs.com](https://nestjs.com/)
- Twitter - [@nestframework](https://twitter.com/nestframework)

## License

Nest is [MIT licensed](LICENSE).
## ที่มา
```https://github.com/Kasidach-Boss/nest```
