# notes-backend

Intalasi penggunaan api notes

## Installasi

```
git init
git clone git@github.com:notfound313/notes-backend.git
cd notes-backend

```

Pembuatan api menggunakan framework HAPI maka perlu adanya penginstalan HAPI

## Installasi npm

```
npm init
npm install @hapi/hapi
npm run start:dev

```

## localhost:5000/notes (GET)

### Header

```
Content-type: aplication/json

```

### Response

```
{
    "status":"success","data":{"notes":[]}
    }

```

## localhost:5000/notes (POST)

### Header

```
Content-type: appliaction/json

```

### Body

```
{
    "title": "Catatan A",
    "tags": ["Android", "Web"],
    "body": "Isi dari catatan A"
}
```

### Response

```
{
    'status':'succes',
    'message':'catatan berhasil ditambah',
    'data':{
        'noteId':'x4EF3B_wPdXm8Nj0'
    }
}
```

## localhost:5000/notes/{id} (GET)

id = x4EF3B_wPdXm8Nj0

### response

```
{
    "status": "succes",
    "data": {
        "note": {
            "id": "x4EF3B_wPdXm8Nj0",
            "createdAt": "2024-04-15T06:41:06.359Z",
            "updatedAt": "2024-04-15T06:41:06.359Z"
        }
    }
}
```

## localhost:5000/notes/{id} (PUT)

### body

```
{
   "title": "Catatan A Revisi",
   "tags": ["Android", "Web"],
   "body": "Isi dari catatan A revisi"
}

```

### Response

```
{
    "status": "succes",
    "message": "Note berhasil diubah"
}
```

## localhost:5000/notes/{id} (DELETE)

```
{
    "status": "success",
    "message": "note berhasil dihapus"
}

```
