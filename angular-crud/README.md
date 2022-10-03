Build the angular-crud schematic:

cd angular-crud
npm install
npm run build
npm pack

Install the needed npm packages:

cd 'project repository'
npm i --no-save ../angular-crud/*.tgz
# or install the latest released version with: npm install -D angular-crud
npm install

NOTE: For Bootstrap and Angular Material, use demo-bootstrap and demo-material in the first command.

Switch to the folder src/app and create a sub-folder hotel with a file model.json. Put the following content into this file:

{ 
    "title": "Hotel",
    "entity": "hotel",
    "api": {
      "url": "http://www.angular.at/api/hotel"
    },
    "filter": [
      "city"
    ],
    "fields": [
      {
        "name": "id",
        "label": "Id",
        "isId": true,
        "readonly": true,
        "type": "number"
      },
      {
        "name": "name",
        "type": "string",
        "label": "Name"
      },
      {
        "name": "city",
        "type": "string",
        "label": "City"
      },
      {
        "name": "stars",
        "type": "string",
        "control": "number",
        "label": "Stars"
      } 
    ]
}