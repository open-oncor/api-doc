[Работа с пациентами](../../patient.md)
=====================================================

### ![POST](../../../../img/post.png) /patient/add

### Examples

**URI** `http://.../patient/add`

**Request**

```json
{
  "patient": {
    "first_name": "Андрей",
    "middle_name": "Вадимович",
    "last_name": "Макаревич",
    "birth_day": "1953-12-11",
    "gender": {
      "id": "1",
      "caption": "М"
    },
    "code": "",
    "blood_type": {
      "id": "I_N",
      "caption": "0(I)Rh-"
    },
    "social_status": {
      "id": "6"
    },
    "company_name": "певец песен ртом",
    "insurance": {
      "insurance_number": "666666"
    },
    "address": {
      "town": "Мытищи",
      "street": "Победы",
      "house": "190",
      "flat": "4",
      "postal_code": "",
      "fias": "",
      "kladr": "",
      "okato": "",
      "med_terr_unq": "",
      "type": {
        "id": "HP",
        "caption": "Адрес регистрации"
      },
      "living_area_type": {
        "id": "0"
      }
    }
  }
}
```

**Response `200`**

```json
{
  "result": [
    {
      "id": "#110:78959",
      "first_name": "Андрей",
      "middle_name": "Вадимович",
      "last_name": "Макаревич",
      "birth_day": "1953-12-11",
      "gender": {
        "id": "2",
        "caption": "Ж"
      },
      "code": "",
      "blood_type": {
        "id": "I_N",
        "caption": "0(I)Rh-"
      },
      "company_name": "певец песен ртом",
      "snils": "",
      "insurance": {
        "insurance_number": "6666666"
      },
      "address": {
        "address": "",
        "federal_code": "",
        "region_code": "",
        "town": "Мытищи",
        "street": "Победы",
        "house": "12",
        "flat": "3",
        "postal_code": "",
        "fias": "",
        "kladr": "",
        "okato": "",
        "med_terr_unq": "",
        "type": {
          "id": "HP",
          "caption": "Адрес регистрации"
        },
        "living_area_type": {
          "id": "1"
        }
      }
    }
  ]
}
```

**Response `422`**

```json
{
  "error": {
    "name": "com.siams.med.api.PatientAlreadyExistsException",
    "message": "Too many patients: 1",
    "uuid": "b145acc8-3fd1-4cb0-bdba-f7532e047cb5"
  }
}
```
