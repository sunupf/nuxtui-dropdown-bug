<template>
  <div>
    <UDropdown :items="cardMenu">
      <UButton :paddded="false" icon="i-heroicons-ellipsis-vertical" variant="ghost" @click="foo(1)"/>
    </UDropdown>
  </div>
</template>

<script setup>
const cardMenu = [
    [
      {
        label: 'Edit',
        icon: 'i-heroicons-pencil-square',
        shortcuts: ['E'],
        click: () => {
            console.log('Edit')
        }
      }, {
        label: 'Duplicate',
        icon: 'i-heroicons-document-duplicate',
        shortcuts: ['D'],
        disabled: true
      }
    ],
    [
      {
        label: 'Delete',
        icon: 'i-heroicons-trash',
        click: () => {
            pageConfig.confirmationDeleteSurvey = true
        }
      }
    ]
]

const foo = (num) => {
  console.log(num)
}
</script>
