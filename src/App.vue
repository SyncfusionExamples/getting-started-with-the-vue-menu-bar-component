<script setup>
 import { MenuComponent as EjsMenu } from "@syncfusion/ej2-vue-navigations";
 const menuDataFields ={
    // text: [ 'continent', 'country', 'language' ],
    // children: [ 'countries', 'languages' ]
    itemId: 'id',
    text: 'text',
    parentId: 'pId'
  };

 const complexData = [
    {
        continent: 'Asia',
        countries: [
            {
                country: 'China',
                languages: [
                    { language: 'Mandarin' },
                    { language: 'Cantonese' }
                ]
            },
            {
                country: 'India',
                languages: [
                    { language: 'Hindi' },
                    { language: 'Tamil' },
                    { language: 'Telugu' }    
                ]
            },
            {
                country: 'Japan',
                languages: [
                    { language: 'Japanese' }
                ]
            }
        ]
    },
    {
        continent: 'Africa',
        countries: [
            {
                country: 'Nigeria',
                languages: [
                    { language: 'English' },
                    { language: 'Hausa' }
                ]
            },
            {
                country: 'Egypt',
                languages: [
                    { language: 'Arabic' }
                ]
            },
            {
                country: 'South Africa',
                languages: [
                    { language: 'Tswana' },
                    { language: 'Swazi' }
                ]
            }
        ]
    },
    {
        continent: 'North America',
        countries: [
            {
                country: 'Canada',
                languages: [
                    { language: 'French' }
                ]
            },
            {
                country: 'Mexico',
                languages: [
                    { language: 'Spanish' }
                ]
            },
            {
                country: 'USA',
                languages: [
                    { language: 'English' }
                ]
            }
        ]
    },
    {
        continent: 'South America',
        countries: [
            {
                country: 'Brazil',
                languages: [
                    { language: 'Portuguese' }
                ]
            },
            {
                country: 'Colombia',
                languages: [
                    { language: 'Spanish' }
                ]
            },
            {
                country: 'Argentina',
                languages: [
                    { language: 'Spanish' }
                ]
            }
        ]
    }
  ];

 const menuItems =  [
{
    text: 'File',
    iconCss: 'em-icons e-file',
    items: [
        { text: 'Open', iconCss: 'em-icons e-open' },
        { text: 'Save', iconCss: 'em-icons e-save' },
        { separator: true},
        { text: 'Exit' }
    ]
},
{
    text: 'Edit',
    iconCss: 'em-icons e-edit',
    items: [
        { text: 'Cut', iconCss: 'em-icons e-cut' },
        { text: 'Copy', iconCss: 'em-icons e-copy' },
        { text: 'Paste', iconCss: 'em-icons e-paste' }
    ]
},
{
    text: 'View',
    items: [
        { text: 'Toolbar' },
        { text: 'Sidebar' }
    ]
},
{
    text: 'Tools',
    items: [
        { text: 'Spelling & Grammar' },
        { text: 'Customize' },
        { text: 'Options' }
    ]
},
{ text: 'Go' },
{ text: 'Help' }
 ];
 const menubarDatasource = [
    { id: 'parent1', text: 'Appliances' },
    { id: 'parent2', text: 'Accessories' },
    { id: 'parent3', text: 'Fashion' },
    { id: 'parent4', text: 'Home & Living' },
    { id: 'parent5', text: 'Entertainment' },

    { id: 'parent6', text: 'Kitchen', pId: 'parent1' },
    { id: 'parent7', text: 'Washing Machine', pId: 'parent1' },
    { id: 'parent8', text: 'Air Conditioners', pId: 'parent1' },

    { id: 'parent9', text: 'Electric Cookers', pId: 'parent6' },
    { id: 'parent10', text: 'Coffee Makers', pId: 'parent6' },
    { id: 'parent11', text: 'Blenders', pId: 'parent6' },

    { id: 'parent12', text: 'Fully Automatic', pId: 'parent7' },
    { id: 'parent13', text: 'Semi Automatic', pId: 'parent7' },

    { id: 'parent14', text: 'Inverter AC', pId: 'parent8' },
    { id: 'parent15', text: 'Split AC', pId: 'parent8' },
    { id: 'parent16', text: 'Window AC', pId: 'parent8' },

    { id: 'parent17', text: 'Mobile', pId: 'parent2' },
    { id: 'parent18', text: 'Computer', pId: 'parent2' },

    { id: 'parent19', text: 'Memory Card', pId: 'parent17' },
    { id: 'parent20', text: 'Power Bank', pId: 'parent17' },

    { id: 'parent21', text: 'Pendrive', pId: 'parent18' },
    { id: 'parent22', text: 'Monitor', pId: 'parent18' },

    { id: 'parent23', text: 'Men', pId: 'parent3' },
    { id: 'parent24', text: 'Women', pId: 'parent3' },

    { id: 'parent25', text: 'Shirts', pId: 'parent23' },
    { id: 'parent26', text: 'Jackets', pId: 'parent23' },
    { id: 'parent27', text: 'Track Suits', pId: 'parent23' },

    { id: 'parent28', text: 'Kurtas', pId: 'parent24' },
    { id: 'parent29', text: 'Salwars', pId: 'parent24' },
    { id: 'parent30', text: 'Sarees', pId: 'parent24' },

    { id: 'parent31', text: 'Furniture', pId: 'parent4' },
    { id: 'parent32', text: 'Decor', pId: 'parent4' },

    { id: 'parent33', text: 'Beds', pId: 'parent31' },
    { id: 'parent34', text: 'Mattresses', pId: 'parent31' },

    { id: 'parent35', text: 'Clocks', pId: 'parent32' },
    { id: 'parent36', text: 'Paintings', pId: 'parent32' },

    { id: 'parent37', text: 'Television', pId: 'parent5' },
    { id: 'parent38', text: 'Home Theatre', pId: 'parent5' }
  ];
 const animationSettings = {
    effect: 'ZoomIn',
    duration: 800
  };
</script>

<template>
  <div style="padding-bottom:300px">
    <ejs-menu :items='menubarDatasource' :fields="menuDataFields" 
    orientation="Vertical" :animationSettings="animationSettings"></ejs-menu>
  </div>
</template>

<style>
@import "../node_modules/@syncfusion/ej2-base/styles/material.css";
@import "../node_modules/@syncfusion/ej2-popups/styles/material.css";
@import "../node_modules/@syncfusion/ej2-navigations/styles/material.css";
@font-face {
    font-family: 'em-icons';
    src: url(data:application/x-font-ttf;charset=utf-8;base64,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) format('truetype');
}
.em-icons { 
    font-family: 'em-icons';
    line-height: 1;
}
.e-menu-wrapper .e-file::before {
    content: '\e700';
}

 .e-menu-wrapper .e-edit::before {
    content: '\e701';
}

.e-menu-wrapper .e-cut::before {
    content: '\e704';
}

.e-menu-wrapper .e-copy::before {
    content: '\e705';
}

.e-menu-wrapper .e-paste::before {
    content: '\e706';
}

.e-menu-wrapper .e-open::before {
    content: '\e702';
}

.e-menu-wrapper .e-save::before {
    content: '\e703';
}
</style>
