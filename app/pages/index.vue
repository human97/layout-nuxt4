<template>
  <div class="min-h-screen bg-[#05060E] text-white px-[10px] py-[45px] md:px-10 md:py-[70px] lg:px-16 lg:py-[100px]">
    <div class="max-w-[1792px] mx-auto">
      <div class="mb-5 lg:mb-[30px] text-center max-w-sm lg:max-w-4xl mx-auto">
        <h1 class="mb-[30px] lg:mb-10 text-[28px] lg:text-[58px] leading-none">
          Проверенные решения для разнообразных задач
        </h1>
        <p class="text-base lg:text-[38px] leading-none">
          Сопровождаем бизнес <br>
          с повышенными требованиями
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-[10px] grid-auto-rows-fr">
        <CardItem
          v-for="(card, index) in cards" 
          :key="index"
          :card="card"
          class="text-red"
          :class="getCardPositionClasses(index)"
        />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">

const cards = [
  { title: 'Консультация и помощь иностранным гражданам в подготовке заявления на разрешение на временное проживание (РВП) и вида на жительство (ВНЖ) в РФ' },
  { title: 'Переводы документов с языков стран СНГ, нотариально заверенные' },
  { title: 'Подача уведомлений о трудовой деятельности и трудовых договоров за иностранных граждан, оплата авансовых платежей за патентщиков' }, 
  { title: 'Рассылка/оповещение сотрудникам' }, 
  { title: 'Организация кол-центра для сотрудников' }, 
  { title: 'Юридические консультации (трудовое, миграционное, налоговое право)' }, 
  { title: 'Оформление ДМС для сотрудников (РФ и иностранцы)' }, 
  { title: 'Сопровождение контрактов с подрядчиками' }, 
  { title: 'Аутсорсинг службы безопасности' } 
];

const getCardPositionClasses = (index: number): string => {
  const remainder = index % 3;
  
  let positionClass = '';

  switch (remainder) {
    case 0:
      positionClass = 'md:col-start-2'; 
      break;
    case 1:
      positionClass = 'md:col-start-1';
      break;
    case 2:
      positionClass = 'md:col-start-3'; 
      break;
  }
  
  return positionClass;
};
</script>