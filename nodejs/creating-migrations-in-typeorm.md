# Creating migrations with typeorm

First, you must create an entity. Like this:

```typescript
import { Entity, PrimaryGeneratedColumn, Column } from 'typeorm';

@Entity()
export default class Service {
  @PrimaryGeneratedColumn('increment')
  id!: number;

  @Column()
  name!: string;

  @Column()
  description!: string;

  @Column()
  value!: number;
}
```

Then, you must config your `ormconfig.json` with your database credentials.

So, you add this line in the *scripts* section of your `package.json`

``` json
"typeorm": "node --require ts-node/register ./node_modules/typeorm/cli.js"
```
> You must have installed the *ts-node* package

Then, run this command in your terminal:

```bash
yarn typeorm migration:generate -n createServices
```
>Replace *createServices* with yor migration action and entity name 

Finally, the created file looks like this:
```typescript
import { MigrationInterface, QueryRunner } from 'typeorm';

export class createServices1600133462355 implements MigrationInterface {
  name = 'createServices1600133462355';

  public async up(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.query(`
    CREATE TABLE "service" ("id" SERIAL NOT NULL, "name" character varying NOT NULL, "description" character varying NOT NULL, "value" integer NOT NULL, CONSTRAINT "PK_85a21558c006647cd76fdce044b" PRIMARY KEY ("id"))`);
  }

  public async down(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.query(`DROP TABLE "service"`);
  }
}

```