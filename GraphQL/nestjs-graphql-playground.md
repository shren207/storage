# nestjs-graphql-playground
> NestJS와 GraphQL을 사용하여 만든 서버 프로젝트인 `nestjs-graphql-playground`를 분석하여 정리

## 특징
- Active Record, Data Mapper 중 Active Record로 작성되었음 (TypeORM)
  - Data Mapper는 어려움
- Code First, Schema First 중 Code First로 작성되었음 (GraphQL)
  - 만약 express를 사용하는 경우에는 Code First로만 작성해야 함
  - GraphQL을 Code First 방식으로 작성할 때, `@ObjectType()` 등의 데코레이터 함수가 사용된다
- GraphQL을 사용해서 NestJS 프로젝트를 만드는 경우, Controller가 필요 없음 (REST API를 사용하는 경우에만 필요함)
- 서버에서 사용하는 DB인 postgres는 local에 직접 설치하지 않고, docker-compose를 사용해서 띄운다
- graphql-upload, mercurius-upload 중 mercurius-upload를 사용함 (파일 업로드)
  - express가 아닌 fastify를 사용하는 경우에는 mercurius-upload의 사용이 강제되는 듯함
