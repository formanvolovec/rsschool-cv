| **Имя и Фамилия**             | Eugene Emelin                                                                 |
|-------------------------------|------------------------------------------------------------------------------|
| **Discord**                   | eugenevolovec                                                                |
| **Краткая информация о себе** | Бывший Full Stack разработчик. После переезда в Польшу временно вне IT. <br> Мотивирован на результат, постоянно учусь и расширяю знания в IT. <br> Командный игрок с сильными коммуникативными навыками, эффективен в офисной среде. |
| **Навыки**                    | **Бэкенд:** <br> NestJS, ExpressJS, Node.js, MongoDB, PostgreSQL, GraphQL, RabbitMQ, Mongoose/TypeORM, REST API, Microservice Architecture, Docker, Azure ADX. <br><br> **Фронтенд:** <br> ReactJS, VueJS, Redux, HTML, CSS, Axios. <br><br> **Языки:** <br> JavaScript, TypeScript. <br><br> **Методологии:** <br> ООП. <br><br> **Инструменты:** <br> Git, Linux, Azure. <br><br> **Софт-скиллы:** <br> Teamwork. |
| **Опыт работы**               | **Full stack NodeJS + VueJS (remote)** <br> *Июнь 2022 - Февраль 2023* <br> **Компания:** NDA (системы домашней безопасности) <br> **Технологии:** <br> Express, Node.js, MongoDB, Redis, Docker, Azure ADX, Microservices, TypeScript, Vue.js <br> **Обязанности:** <br> Разработка Full Stack приложений на микросервисной архитектуре. <br> Коммуникация на английском. <br><br> **Full stack NodeJS + ReactJS (remote, freelance)** <br> *Сентябрь 2021 - Ноябрь 2021* <br> **Компания:** NDA <br> **Технологии:** <br> Express, MongoDB, GraphQL, Yoga, ReactJS, HTML, CSS, TypeScript <br> **Обязанности:** <br> Разработка веб-сервиса для создания/хранения заметок. <br><br> **Full stack NodeJS + ReactJS (remote)** <br> *Июнь 2021 - Август 2021* <br> **Компания:** NDA (платформа аренды недвижимости) <br> **Технологии:** <br> Nest.Js, PostgreSQL, REST API, Microservices, ReactJS, Redux, HTML, CSS, TypeScript. |
| **Образование**               | **Full Stack NodeJS + ReactJS** <br> *IntexSoft, Гродно, Беларусь* <br> *Март 2022* <br> **Технологии:** <br> NestJS, PostgreSQL, REST API, Docker, TypeScript, Microservices, React, Redux, HTML, CSS, Axios. <br><br> **Software technician** <br> *Колледж бизнеса и права, Гродно, Беларусь* <br> *Июнь 2015* |
| **Английский язык**           | **Уровень:** B1                                                             |
| **Пример кода**               | 
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
                                                 

