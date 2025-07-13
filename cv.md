# Eugene Emelin
**Full stack JavaScript web developer**  
Discord: eugenevolovec | Telegram: jack_spancer | email: formanvolovec@gmail.com

## Summary  
Full Stack developer. After moving to Poland, temporarily out of IT. Motivated by results, constantly learning and expanding my knowledge in IT. Team player with strong communication skills, effective in an office environment.

## Skills  
- NestJS
- ExpressJS
- JavaScript
- TypeScript
- MongoDB
- PostgreSQL
- GraphQL
- RabbitMQ
- Mongoose/TypeORM
- ReactJS
- VueJS
- Azure
- Git
- Object oriented programming
- REST
- Linux

## Code examples  
```
  async search(searchBookDto: SearchBookDto) {
    const { limit, offset, ...rest } = searchBookDto;
    const qb = this.bookRepository.createQueryBuilder('b');
    qb.limit(+searchBookDto.limit || 8);
    qb.offset(offset <= 1 ? 0 : limit * (offset - 1));
    const params = {};
    Object.keys(rest).forEach((key) => {
      qb.andWhere(`b.${key} ILIKE :${key}`);
      params[key] = `%${searchBookDto[key]}%`;
    });
    qb.setParameters(params);
    const [items, total] = await qb.getManyAndCount();
    const mappedItems = items.map((book) => {
      return { ...book, description: book.description.substring(0, 50) };
    });
    return { items: mappedItems, total };
  }
```

## Employers
**“NDA” role: Full stack NodeJS + VueJS | remote | JUN 2022 - FEB 2023** 

**Technologies:**
- Express
- NodeJs
- MongoDB
- Redis
- Docker
- Azure ADX
- Microservice
- TypeScript
- VueJs.

The company develops software for its own home security systems.
Full stack application development. Project based on Microservices
architecture.

**“NDA” |role: Full stack NodeJS + ReactJS | remote, freelance | SEP 2021 - NOV 2021**

**Technologies:**
- TypeScript
- Express
- MongoDB
- GraphQL
- Yoga
- ReactJs
- HTML
- CSS

Developed system like web service and a set of software for creating
and storing notes.


**“NDA” role: Full stack NodeJS + ReactJS| remote | JUN 2021 - AUG 2021**

**Technologies:**
- NestJs
- PostgreSQL
- REST API
- Microservice Architecture Development
- ReactJs
- Redux
- HTML
- CSS
- TypeScript.

The company develops Platform for selling or renting real estate.

## Education  
### Software technician
**Private educational institution “College of Business and Law” | 2015**
### Courses 
**Intexsoft - JS / Full Stack NodeJS + ReactJS | 2022**


## Languages  
- **Russian**: Native  
- **English**: Intermediate (B1)  

--- 
