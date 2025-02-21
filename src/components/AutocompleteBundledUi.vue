<template>
    <div id="autocomplete-container"></div>
</template>
  
<script>
  import CioAutocomplete from '@constructor-io/constructorio-ui-autocomplete/constructorio-ui-autocomplete-bundled';
  import '@constructor-io/constructorio-ui-autocomplete/styles.css';
  
  export default {
    mounted() {
      CioAutocomplete({
        selector: '#autocomplete-container',
      apiKey: process.env.VUE_APP_API_KEY,
        onSubmit: (submitEvent) => console.dir(submitEvent),
        autocompleteClassName: 'cio-autocomplete full-example-autocomplete-styles',
        placeholder: 'What can we help you find?',
        advancedParameters: {
          displaySearchSuggestionImages: true,
          displaySearchSuggestionResultCounts: true,
          numTermsWithGroupSuggestions: 6
        },
        sections: [
          {
            indexSectionName: 'Search Suggestions',
            numResults: 8,
            displaySearchTermHighlights: true
          },
          {
            indexSectionName: 'Products',
            numResults: 6,
            displaySearchTermHighlights: true
          }
        ],
      });
    }
  };
</script>