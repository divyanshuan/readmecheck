## Welcome To BytcodeLearners

This API Documentation help you to use all api provided by BytecodeLearners server. This will help you in further development and the changes in BytecodeLearners Official website.

> **Note**
> The server url may change according to the hosting contact web administrator if url is not working.
> current url : http://bytecodelearners.cuh.ac.in/

**Info**
some url requires `Authentication` for access for that get token first [token](#gettoken).

## APIs

- [Admin](#admin)
- [Members](#members)
- [Event Gallery](#eventgallery)
- [Upcoming Event](#upcomingevent)
- [Previous Event Gallery](#prevevntgallery)

<a name='admin'></a>

# Admin

> **Note**
> There will be only one Admin account for the BytecodeLearners server.

This section is intended for the Team Manager of BytecodeLearners Club, who has full access to the server. Some APIs within this section require authentication, and access will be limited to the Team Manager. For further development, the Team Manager and Technical Head will be responsible for sharing credentials and ensuring a stable and secure update process.

### 1. Login

<a name="gettoken"></a>

- Description: This API is responsible for generating an `access_token` (JWT bearer) that will be essential for accessing all APIs that require authentication.
- Url: `/api/user/login`
- Method: `POST`
- Authorization: `Not required`

- Body: form-data

  ```js
  {
      email:"<admin mail>",
      pssword:""

  }
  ```

### 2. Change Regristration open

- Description: This API is responsible for determining whether registration for current batch students is being accepted or not.
- Url: `/api/user/setreg`
- Method: `POST`
- Authorization: `required`
- Authorization: "Bearer `acces_token`"

- Body: form-data

  ```js
  {
      email:"<admin mail>",
      is_registration_open: True/False

  }
  ```

  > True: Registration for members is open for the current batch.
  > False: Registration for members is not currently being accepted.

## 3. Register Admin

- Description:This API endpoint is responsible for adding an admin account.

  > **Note**
  > This route will be disable on the server.for localhost uncomment this route from routes/api.php

- Url: `/api/user/register`
- Method: `POST`
- Authorization: `Not required`

- Body: form-data

  ```js
  {
      name:"< name>"
      email:"<email>",
      password:"<password>"
      is_registration_open:False

  }
  ```

  > only one admin should be added.
  > True: Registration for members is open for the current batch.
  > False: Registration for members is not currently being accepted.

<a name='members'></a>

# Members

This section is for adding BytecodeLearners members' information, as well as deleting and updating it. This information will be displayed on the BytecodeLearners official website.

### 1. Get all Active Members

- Description: This API endpoint retrieves a list of currently active BytecodeLearners members for display on the official website.
- Url: `/api/member/getactive`
- Method: `GET`
- Authorization: `Not required`

### 2. Get all Active Members by batch

- Description: This API endpoint retrieves a list of currently active BytecodeLearners members of given batch for display on the official website.
- Url: `/api/member/getactive/batch/{batch}`
- Method: `GET`
- Authorization: `Not required`

### 3. Get all Members

- Description: This API endpoint retrieves a list of all (currently active or inactive) BytecodeLearners members inactive member include new registrations.

- Url: `/api/member/getactive`
- Method: `GET`
- Authorization: `required`
- Authorization: "Bearer `acces_token`"

## 3. Add Member / Register Member

- Description:This API endpoint is responsible for registration for new members or adding new members .
- Url: `/api/member/add`
- Method: `POST`
- Authorization: `Not required`

- Body: form-data

  ```js
  {
  firstName: "required",
  lastName: "required",
  email: "required",
  mobile: "required",
  batch: "required",
  isActive: "False by default",
  image: "profile.jpg",
  github: "required",
  linkedin: "required",
  facebook: "nullable",
  instagram: "nullable",
  youtube: "nullable",
  twitter: "nullable"
  };
  ```
