# Web-SangTaoTruyen
## Api của web
"paths": {
"/api/author/getAuthor": {
"get": {
"tags": [
"author"
],
"parameters": [
{
"name": "author",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "type",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/author/check": {
"get": {
"tags": [
"author"
],
"parameters": [
{
"name": "author",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/bookmark/test": {
"get": {
"tags": [
"bookmark"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/bookmark/count/{novelId}": {
"get": {
"tags": [
"bookmark"
],
"parameters": [
{
"name": "novelId",
"in": "path",
"required": true,
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/bookmark/detail": {
"get": {
"tags": [
"bookmark"
],
"parameters": [
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1000000
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/bookmark": {
"get": {
"tags": [
"bookmark"
],
"parameters": [
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1000000
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/bookmark/addb": {
"post": {
"tags": [
"bookmark"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/BookmarkCreate"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/BookmarkCreate"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/BookmarkCreate"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/bookmark/rmb/{id}": {
"delete": {
"tags": [
"bookmark"
],
"parameters": [
{
"name": "id",
"in": "path",
"required": true,
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/bookmark/remove/{novelId}": {
"delete": {
"tags": [
"bookmark"
],
"parameters": [
{
"name": "novelId",
"in": "path",
"required": true,
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/category": {
"get": {
"tags": [
"category"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/category/addcate": {
"post": {
"tags": [
"category"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/CategoryCreate"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/CategoryCreate"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/CategoryCreate"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/category/test": {
"get": {
"tags": [
"category"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/chapter/CrawlApiChapter": {
"get": {
"tags": [
"chapter"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/chapter/testHangfire": {
"post": {
"tags": [
"chapter"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/chapter": {
"get": {
"tags": [
"chapter"
],
"parameters": [
{
"name": "NovelId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
},
{
"name": "sort",
"in": "query",
"schema": {
"type": "boolean",
"default": false
}
},
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 10
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/chapter/getNewUpdate": {
"get": {
"tags": [
"chapter"
],
"parameters": [
{
"name": "sort",
"in": "query",
"schema": {
"type": "boolean",
"default": true
}
},
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 10
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/chapter/getNewChapter": {
"get": {
"tags": [
"chapter"
],
"parameters": [
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 12
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/chapter/getUpdate": {
"get": {
"tags": [
"chapter"
],
"parameters": [
{
"name": "idChapter",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/chapter/getMyChapter": {
"get": {
"tags": [
"chapter"
],
"parameters": [
{
"name": "NovelId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
},
{
"name": "NameChapter",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "Sort",
"in": "query",
"schema": {
"type": "boolean"
}
},
{
"name": "IsSort",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
},
{
"name": "Select",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 10
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/chapter/testGetListChapter": {
"get": {
"tags": [
"chapter"
],
"parameters": [
{
"name": "NovelId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/chapter/getReadChapter": {
"get": {
"tags": [
"chapter"
],
"parameters": [
{
"name": "Slug",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "ChapterId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/chapter/unLock": {
"post": {
"tags": [
"chapter"
],
"parameters": [
{
"name": "IdChapter",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/chapter/addc": {
"post": {
"tags": [
"chapter"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/ChapterVM"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/ChapterVM"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/ChapterVM"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/chapter/restore/{idChapter}": {
"put": {
"tags": [
"chapter"
],
"parameters": [
{
"name": "idChapter",
"in": "path",
"required": true,
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/chapter/remove/{idChapter}": {
"delete": {
"tags": [
"chapter"
],
"parameters": [
{
"name": "idChapter",
"in": "path",
"required": true,
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/chapter/update/{idChapter}": {
"put": {
"tags": [
"chapter"
],
"parameters": [
{
"name": "idChapter",
"in": "path",
"required": true,
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/ChapterUpdate"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/ChapterUpdate"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/ChapterUpdate"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/chapter/updateVip/{novelId}": {
"put": {
"tags": [
"chapter"
],
"parameters": [
{
"name": "novelId",
"in": "path",
"required": true,
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/UpdateChapterVip"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/UpdateChapterVip"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/UpdateChapterVip"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/chapter/removeChapter/{idChapter}": {
"delete": {
"tags": [
"chapter"
],
"parameters": [
{
"name": "idChapter",
"in": "path",
"required": true,
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/comment": {
"get": {
"tags": [
"comment"
],
"parameters": [
{
"name": "Slug",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "sort",
"in": "query",
"schema": {
"type": "boolean",
"default": true
}
},
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 100000
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/comment/reply": {
"get": {
"tags": [
"comment"
],
"parameters": [
{
"name": "commentId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
},
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 100000
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/comment/addcm": {
"post": {
"tags": [
"comment"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/CommentCreate"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/CommentCreate"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/CommentCreate"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/comment/addcmc": {
"post": {
"tags": [
"comment"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/CommentChildrenVM"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/CommentChildrenVM"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/CommentChildrenVM"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/comment/updatecm": {
"put": {
"tags": [
"comment"
],
"parameters": [
{
"name": "id",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/CommentCreate"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/CommentCreate"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/CommentCreate"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/comment/updatecmc": {
"put": {
"tags": [
"comment"
],
"parameters": [
{
"name": "id",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/CommentChildrenVM"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/CommentChildrenVM"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/CommentChildrenVM"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/comment/removecm": {
"delete": {
"tags": [
"comment"
],
"parameters": [
{
"name": "id",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/comment/removecmc": {
"delete": {
"tags": [
"comment"
],
"parameters": [
{
"name": "id",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/comment/removeAll": {
"delete": {
"tags": [
"comment"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/donate": {
"get": {
"tags": [
"donate"
],
"parameters": [
{
"name": "NovelId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/donate/addDonnate": {
"post": {
"tags": [
"donate"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/DonateVM"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/DonateVM"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/DonateVM"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/donate/UpdateDonante": {
"put": {
"tags": [
"donate"
],
"parameters": [
{
"name": "id",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
},
{
"name": "mes",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/draft": {
"get": {
"tags": [
"draft"
],
"parameters": [
{
"name": "id",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
},
"post": {
"tags": [
"draft"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/DraftVM"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/DraftVM"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/DraftVM"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/draft/getListDraft": {
"get": {
"tags": [
"draft"
],
"parameters": [
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 10
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/draft/upChapter": {
"post": {
"tags": [
"draft"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/DraftConvertChapter"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/DraftConvertChapter"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/DraftConvertChapter"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/draft/delete/{id}": {
"delete": {
"tags": [
"draft"
],
"parameters": [
{
"name": "id",
"in": "path",
"required": true,
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/editorNominations": {
"get": {
"tags": [
"editorNominations"
],
"responses": {
"200": {
"description": "Success"
}
}
},
"post": {
"tags": [
"editorNominations"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/NovelEditorNominationsVM"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/NovelEditorNominationsVM"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/NovelEditorNominationsVM"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/image/{keyname}": {
"get": {
"tags": [
"image"
],
"parameters": [
{
"name": "keyname",
"in": "path",
"required": true,
"schema": {
"type": "string",
"nullable": true
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/likeNovel": {
"get": {
"tags": [
"likeNovel"
],
"parameters": [
{
"name": "useId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 0
}
},
{
"name": "novelId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 0
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/likeNovel/addlike": {
"post": {
"tags": [
"likeNovel"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/LikeCreate"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/LikeCreate"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/LikeCreate"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/likeNovel/removelike": {
"delete": {
"tags": [
"likeNovel"
],
"parameters": [
{
"name": "idChapter",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/nominations/currentUser": {
"get": {
"tags": [
"nominations"
],
"parameters": [
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 100
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/nominations": {
"get": {
"tags": [
"nominations"
],
"parameters": [
{
"name": "useId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 0
}
},
{
"name": "novelId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 0
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/nominations/userCurrentUpdateEveryday": {
"post": {
"tags": [
"nominations"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/nominations/addNomi": {
"post": {
"tags": [
"nominations"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/NominationsCreate"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/NominationsCreate"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/NominationsCreate"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/nominations/rm/{id}": {
"delete": {
"tags": [
"nominations"
],
"parameters": [
{
"name": "id",
"in": "path",
"required": true,
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/notification/newNotifi": {
"get": {
"tags": [
"notification"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/notification": {
"get": {
"tags": [
"notification"
],
"parameters": [
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1000000
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/notification/createNotifi": {
"post": {
"tags": [
"notification"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/NotificationVM"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/NotificationVM"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/NotificationVM"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/notification/UpdateNotifi": {
"put": {
"tags": [
"notification"
],
"parameters": [
{
"name": "id",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
},
{
"name": "status",
"in": "query",
"schema": {
"type": "boolean",
"default": true
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/notification/UpdateAllNotifi": {
"put": {
"tags": [
"notification"
],
"parameters": [
{
"name": "status",
"in": "query",
"schema": {
"type": "boolean",
"default": true
}
},
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1000000
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/notification/RemoveNotifi": {
"delete": {
"tags": [
"notification"
],
"parameters": [
{
"name": "id",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/testDemNgay": {
"get": {
"tags": [
"novel"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/getName": {
"get": {
"tags": [
"novel"
],
"parameters": [
{
"name": "NovelId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/getListNovelSimplify": {
"get": {
"tags": [
"novel"
],
"parameters": [
{
"name": "novelId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/TestGetNovel/Test": {
"get": {
"tags": [
"novel"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/CrawlDataFrom": {
"get": {
"tags": [
"novel"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/statisticChar": {
"get": {
"tags": [
"novel"
],
"parameters": [
{
"name": "typeStatistics",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "typeTime",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "NovelId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/statistic": {
"get": {
"tags": [
"novel"
],
"parameters": [
{
"name": "novelId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/statisticBasic": {
"get": {
"tags": [
"novel"
],
"parameters": [
{
"name": "novelId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/SetPublicNovel": {
"get": {
"tags": [
"novel"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/{Slug}": {
"get": {
"tags": [
"novel"
],
"parameters": [
{
"name": "Slug",
"in": "path",
"required": true,
"schema": {
"type": "string",
"nullable": true
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/getEdit": {
"get": {
"tags": [
"novel"
],
"parameters": [
{
"name": "NovelId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/topNominations/{novelId}": {
"get": {
"tags": [
"novel"
],
"parameters": [
{
"name": "novelId",
"in": "path",
"required": true,
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/getAllNovelOfUserCurrent": {
"get": {
"tags": [
"novel"
],
"parameters": [
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 10
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/getAllNovel": {
"get": {
"tags": [
"novel"
],
"parameters": [
{
"name": "search",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "userId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
},
{
"name": "category",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "sortHot",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "sortView",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "sortNominations",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "sortDonate",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "sortLike",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "sortComment",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "sortReview",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "sortChapter",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "sortTypeTime",
"in": "query",
"schema": {
"type": "string",
"default": "month",
"nullable": true
}
},
{
"name": "sortTime",
"in": "query",
"schema": {
"type": "string",
"default": "update-des",
"nullable": true
}
},
{
"name": "chapter",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 0
}
},
{
"name": "status",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": -1
}
},
{
"name": "properties",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": -1
}
},
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 100000
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/getAllMyNovel": {
"get": {
"tags": [
"novel"
],
"parameters": [
{
"name": "search",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 10
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/images/{keyname}": {
"get": {
"tags": [
"novel"
],
"parameters": [
{
"name": "keyname",
"in": "path",
"required": true,
"schema": {
"type": "string",
"nullable": true
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/create": {
"post": {
"tags": [
"novel"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/NewNovel"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/NewNovel"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/NewNovel"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/nameCheck": {
"get": {
"tags": [
"novel"
],
"parameters": [
{
"name": "name",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/novel/update/{id}": {
"put": {
"tags": [
"novel"
],
"parameters": [
{
"name": "id",
"in": "path",
"required": true,
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/NovelUpdate"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/NovelUpdate"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/NovelUpdate"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/report/nomination": {
"get": {
"tags": [
"report"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/report/comment": {
"get": {
"tags": [
"report"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/report/addnomination": {
"post": {
"tags": [
"report"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/ReportNominationVM"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/ReportNominationVM"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/ReportNominationVM"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/report/addComment": {
"post": {
"tags": [
"report"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/ReportCommentVM"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/ReportCommentVM"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/ReportCommentVM"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/review": {
"get": {
"tags": [
"review"
],
"parameters": [
{
"name": "novelId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
},
{
"name": "userId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
},
{
"name": "sort",
"in": "query",
"schema": {
"type": "boolean",
"default": true
}
},
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 100000
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/review/total": {
"get": {
"tags": [
"review"
],
"parameters": [
{
"name": "novelId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/review/reviewUserCurrent/{novelId}": {
"get": {
"tags": [
"review"
],
"parameters": [
{
"name": "novelId",
"in": "path",
"required": true,
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/review/reply": {
"get": {
"tags": [
"review"
],
"parameters": [
{
"name": "reviewId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
},
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 100000
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/review/addrv": {
"post": {
"tags": [
"review"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/ReviewVM"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/ReviewVM"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/ReviewVM"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/review/addrvc": {
"post": {
"tags": [
"review"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/ReviewChildren"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/ReviewChildren"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/ReviewChildren"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/review/updaterv/{novelId}": {
"put": {
"tags": [
"review"
],
"parameters": [
{
"name": "novelId",
"in": "path",
"required": true,
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/ReviewVM"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/ReviewVM"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/ReviewVM"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/review/updatervc": {
"put": {
"tags": [
"review"
],
"parameters": [
{
"name": "id",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/ReviewChildren"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/ReviewChildren"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/ReviewChildren"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/review/removerv": {
"delete": {
"tags": [
"review"
],
"parameters": [
{
"name": "id",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user": {
"get": {
"tags": [
"user"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/checkVerify": {
"get": {
"tags": [
"user"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/userCurrentInfo": {
"get": {
"tags": [
"user"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/profile/{userName}": {
"get": {
"tags": [
"user"
],
"parameters": [
{
"name": "userName",
"in": "path",
"required": true,
"schema": {
"type": "string",
"nullable": true
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/detailsInfo": {
"get": {
"tags": [
"user"
],
"parameters": [
{
"name": "userId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/currentUser": {
"get": {
"tags": [
"user"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/info": {
"get": {
"tags": [
"user"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/testmahoa": {
"get": {
"tags": [
"user"
],
"parameters": [
{
"name": "passWord",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/addu": {
"post": {
"tags": [
"user"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/UserCreate"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/UserCreate"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/UserCreate"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/Login": {
"post": {
"tags": [
"user"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/LoginVM"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/LoginVM"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/LoginVM"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/RenewToken": {
"post": {
"tags": [
"user"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/TokenModel"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/TokenModel"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/TokenModel"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/LogOut": {
"post": {
"tags": [
"user"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/updateUserInfo": {
"put": {
"tags": [
"user"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/UserInfoCurrent"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/UserInfoCurrent"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/UserInfoCurrent"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/updatePassword": {
"put": {
"tags": [
"user"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/UpdatePassword"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/UpdatePassword"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/UpdatePassword"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/updateEmail": {
"put": {
"tags": [
"user"
],
"parameters": [
{
"name": "newEmail",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/getVerifyEmail": {
"get": {
"tags": [
"user"
],
"parameters": [
{
"name": "hots",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "web",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/confirmEmail": {
"post": {
"tags": [
"user"
],
"parameters": [
{
"name": "token",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/forgotPassword": {
"post": {
"tags": [
"user"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/ForgotPassword"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/ForgotPassword"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/ForgotPassword"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/newPassword": {
"post": {
"tags": [
"user"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/ResetPasswordOfEmail"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/ResetPasswordOfEmail"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/ResetPasswordOfEmail"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/SendEMail": {
"post": {
"tags": [
"user"
],
"parameters": [
{
"name": "toEmail",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "body",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "subject",
"in": "query",
"schema": {
"type": "string",
"nullable": true
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/user/registerCreator": {
"get": {
"tags": [
"user"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/viewed/CountView": {
"get": {
"tags": [
"viewed"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/viewed/updateTestView": {
"get": {
"tags": [
"viewed"
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/viewed": {
"get": {
"tags": [
"viewed"
],
"parameters": [
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 100000
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/viewed/detail/{userName}": {
"get": {
"tags": [
"viewed"
],
"parameters": [
{
"name": "userName",
"in": "path",
"required": true,
"schema": {
"type": "string",
"nullable": true
}
},
{
"name": "page",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 1
}
},
{
"name": "limit",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 100000
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/viewed/infoBasic": {
"get": {
"tags": [
"viewed"
],
"parameters": [
{
"name": "useId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 0
}
},
{
"name": "novelId",
"in": "query",
"schema": {
"type": "integer",
"format": "int32",
"default": 0
}
},
{
"name": "viewType",
"in": "query",
"schema": {
"type": "string",
"default": "all",
"nullable": true
}
}
],
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/api/viewed/addView": {
"post": {
"tags": [
"viewed"
],
"requestBody": {
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/ViewedCreate"
}
},
"text/json": {
"schema": {
"$ref": "#/components/schemas/ViewedCreate"
}
},
"application/*+json": {
"schema": {
"$ref": "#/components/schemas/ViewedCreate"
}
}
}
},
"responses": {
"200": {
"description": "Success"
}
}
}
},
"/WeatherForecast": {
"get": {
"tags": [
"WeatherForecast"
],
"responses": {
"200": {
"description": "Success",
"content": {
"text/plain": {
"schema": {
"type": "array",
"items": {
"$ref": "#/components/schemas/WeatherForecast"
}
}
},
"application/json": {
"schema": {
"type": "array",
"items": {
"$ref": "#/components/schemas/WeatherForecast"
}
}
},
"text/json": {
"schema": {
"type": "array",
"items": {
"$ref": "#/components/schemas/WeatherForecast"
}
}
}
}
}
}
}
}
},
