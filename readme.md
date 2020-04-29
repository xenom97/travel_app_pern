Travel Web App Backend

- PostgreSql (Sequelize)
- Express
- Node

1. Get start

- sequelize db:create
- sequelize db:migrate
- npm start

API Documentation<br>
**URL**

- ("/admin")

  - ("/register") <br>
    **Method**
    `POST`<br>
    **Params**<br>
    `none`<br>
    **Query (req.query)**<br>
    `none`<br>
    **Data (req.body)**<br>

    ```json
    { username[string], password[string], confirmPassword[string]}
    ```

    **Success Responses**<br>
    **code**<br>
    status = 201

    **content**

    ```json
    {
    	"success": true,
    	"code": 201,
    	"message": "Register Success",
    	"result": Username[string]
    }
    ```

    **Error Responses**<br>

    **code**<br>
    status = 400 (will change later)

    **content**

    ```json
    {
    	"success": false,
    	"code": 400,
    	"message": "SequelizeValidationError",
    	"result": ["username already exists"]
    }
    ```

  - ("/login")
    **Method**
    `POST`<br>
    **Params**<br>
    `none`<br>
    **Query (req.query)**<br>
    `none`<br>
    **Data (req.body)**<br>

    ```json
    { username[string], password[string]}
    ```

    **Success Responses**<br>
    **code**<br>
    status = 200

    **content**

    ```json
    {
    	"success": true,
    	"code": 200,
    	"message": "Login Success",
    	"result": JWT_TOKEN[string]
    }
    ```

    **Error Responses**<br>

    **code**<br>
    status = 400 (will change later)

    **content**

    ```json
    {
    	"success": false,
    	"code": 400,
    	"message": "incorrect username/password",
    	"result": []
    }
    ```

- ("/destinations")

  - ("/") <br>
    **Method**
    `GET`<br>
    **Params**<br>
    `none`<br>
    **Query (req.query)**<br>
    `none`<br>
    **Data (req.body)**<br>
    `none`<br>

    **Success Responses**<br>
    **code**<br>
    status = 200

    **content**

    ```json
    {
    	"success": true,
    	"code": 200,
    	"message": "",
    	"result": destinations[array]
    }
    ```

    **Error Responses**<br>

    **code**<br>
    status = 400

    **content**

    ```json
    {
    	"success": false,
    	"code": 401,
    	"message": "unauthorized",
    	"result": []
    }
    ```
