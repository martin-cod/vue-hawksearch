<template>
    <div class="hawk__searchBox" @click="onClick">
        <div v-if="imageSearchVisible" class="image-search-field">
            <h3>Image Search</h3>
            <button @click="closeImageSearch" class="close-image-search-btn"><svg fill="none" height="14" viewBox="0 0 14 14" width="14" xmlns="http://www.w3.org/2000/svg"><path clip-rule="evenodd" d="m13.3715.638911c-.3944-.394388-1.0314-.394388-1.4258 0l-4.94505 4.934899-4.94501-4.945012c-.39439-.394387-1.03148-.394387-1.425865 0-.394388.394392-.394388 1.031472 0 1.425862l4.945015 4.94501-4.945015 4.94503c-.394388.3944-.394388 1.0315 0 1.4259.394385.3943 1.031475.3943 1.425865 0l4.94501-4.94506 4.94505 4.94506c.3944.3943 1.0314.3943 1.4258 0 .3944-.3944.3944-1.0315 0-1.4259l-4.94499-4.94503 4.94499-4.94501c.3843-.38427.3843-1.03147 0-1.415749z" fill="#3c4043" fill-rule="evenodd"/></svg></button>

            <span class="hawk__uploadImage">
                <svg fill="none" height="78" viewBox="0 0 92 78" width="92" xmlns="http://www.w3.org/2000/svg"><g fill="#000"><path d="m51.875 14.375h-3.125v9h3.125z"/><path d="m51.875 9v-1.125c0-4.125-3.375-7.5-7.5-7.5h-1.125v3.125h1.125c2.375 0 4.375 2 4.375 4.375v1.125z"/><path d="m37.875 48.875h-9v3.125h9z"/><path d="m23.375 48.875h-9v3.125h9z"/><path d="m3.5 28.875h-3.125v9h3.125z"/><path d="m3.5 14.375h-3.125v9h3.125z"/><path d="m7.875 52h1.125v-3.125h-1.125c-2.375 0-4.375-2-4.375-4.375v-1.125h-3.125v1.125c0 4.125 3.375 7.5 7.5 7.5z"/><path d="m7.875 3.5h1.125v-3.125h-1.125c-4.125 0-7.5 3.375-7.5 7.5v1.125h3.125v-1.125c0-2.375 2-4.375 4.375-4.375z"/><path d="m23.375.375h-9v3.125h9z"/><path d="m37.875.375h-9v3.125h9z"/><path d="m32.6249 25.5c.875 0 1.5-.625 1.5-1.5 0-.5-.25-1-.625-1.25l-6.25-4.75c-.5-.5-1.375-.5-1.875 0l-6.25 4.75c-.625.5-.75 1.5-.25 2.125s1.5.75 2.125.25l3.875-2.75v11.25c0 .875.625 1.5 1.5 1.625h.25c.75-.125 1.375-.75 1.375-1.5v-11.25l3.875 2.75s.375.25.75.25z"/><path d="m85.375 27h-38.125c-1.625 0-3.25.625-4.375 1.875-1.25 1-1.875 2.625-1.875 4.25v38.125c0 1.625.625 3.25 1.875 4.375 1.125 1.125 2.75 1.875 4.375 1.875h38.125c1.625 0 3.25-.625 4.375-1.875s1.875-2.75 1.875-4.375v-38.125c0-1.625-.625-3.25-1.875-4.375s-2.625-1.75-4.375-1.75zm3.375 44.375c0 .875-.375 1.75-1 2.375s-1.5 1-2.375 1h-38.125c-.875 0-1.75-.375-2.375-1s-1-1.5-1-2.375v-6.5l5.75-5.75 6.125 6.125c.125.125.25.25.5.375.5.25 1.125.125 1.625-.375l15.625-15.75 15.25 15.25zm0-10.75-14.25-14.125c-.125-.125-.25-.25-.5-.375-.375-.125-.75-.125-1.125 0-.125.125-.375.125-.5.375l-15.625 15.625-6.125-6.125c-.25-.25-.625-.375-1-.375s-.75.125-1 .375l-4.75 4.75v-27.5c0-.875.375-1.75 1-2.375s1.5-1 2.375-1h38.125c.875 0 1.75.375 2.375 1s1 1.5 1 2.375z"/><path d="m60.625 43.125c.125-.875-.125-1.75-.625-2.5s-1.25-1.25-2.125-1.5c-.375-.125-.75-.125-1.125-.125-.5 0-1 .125-1.5.25-.875.375-1.5 1-1.875 1.75s-.5 1.75-.375 2.5c.125.875.625 1.625 1.375 2.25.625.5 1.5.875 2.375.875 1 0 2-.375 2.75-1.125.625-.75 1-1.5 1.125-2.375z"/></g></svg>
            </span>

            <label class="custom-file-upload">
                <svg fill="none" height="16" viewBox="0 0 19 16" width="19" xmlns="http://www.w3.org/2000/svg"><g fill="#fff"><path clip-rule="evenodd" d="m4.8242 4.67039c-2.40242.09031-4.324591 2.04826-4.324591 4.4475 0 2.45641 2.015861 4.45051 4.498161 4.45051h1.19578v-1.188h-1.19578c-1.82008 0-3.29752-1.4619-3.29752-3.26248 0-1.80109 1.4773-3.26311 3.29752-3.26311.28587 0 .57213.03635.85664.06007.2761-2.27703 1.6452-4.2274 4.24099-4.2274 2.3189 0 4.2021 1.86352 4.2021 4.15828 0 .61416.0299.59957 0 1.35987.428 0 3.0015.38962 3.0015 2.79857 0 1.3116-1.0757 2.3761-2.4012 2.3761h-1.8009v1.1881h1.8009c1.9875 0 3.6018-1.5974 3.6018-3.5642 0-1.77806-1.3183-3.25362-3.04-3.52084.0252-.20911.0385-.4218.0385-.63739 0-2.95058-2.4211-5.346361-5.4027-5.346361-2.57412 0-4.72955 1.784981-5.2712 4.170781z" fill-rule="evenodd"/><path d="m6.77989 10.6213-.84545-.80847 3.57385-3.39869 3.55671 3.40094-.8479.80632-2.105-2.01249-.0067 7.09039-1.21236-.0011.00665-7.0933z"/><path clip-rule="evenodd" d="m4.70436 4.52617c.59779-2.39767 2.78637-4.176561 5.39104-4.176561 3.063 0 5.5527 2.461461 5.5527 5.496361 0 .17326-.0083.34465-.0243.51383 1.723.33492 3.0258 1.83902 3.0258 3.6444 0 2.0511-1.6829 3.7142-3.7518 3.7142h-1.9509v-1.4881h1.9509c1.2441 0 2.2512-.9988 2.2512-2.2261 0-1.13791-.6023-1.79362-1.2647-2.17244-.671-.38371-1.3949-.47613-1.5868-.47613h-.156l.0061-.15589c.0187-.47582.0139-.63978.0077-.85106-.0036-.12569-.0078-.26812-.0078-.50292 0-2.21043-1.8145-4.00828-4.0521-4.00828-1.25632 0-2.20698.47026-2.87934 1.21066-.6754.74375-1.07743 1.76889-1.21274 2.88479l-.01739.14343-.14397-.012c-.07656-.00638-.15177-.01349-.22605-.02051-.21023-.01987-.41305-.03904-.61814-.03904-1.73886 0-3.14752 1.39633-3.14752 3.11311 0 1.71618 1.40877 3.11248 3.14752 3.11248h1.34578v1.488h-1.34578c-2.56363 0-4.648161-2.0598-4.648161-4.60051 0-2.44343 1.926971-4.44176 4.354751-4.59172zm5.39104-3.876561c-2.50352 0-4.59866 1.735961-5.12492 4.053991l-.02551.11236-.11514.00433c-2.32356.08734-4.180221 1.98073-4.180221 4.2976 0 2.37201 1.947181 4.30051 4.348161 4.30051h1.04578v-.888h-1.04578c-1.90141 0-3.44752-1.5276-3.44752-3.41248 0-1.88541 1.54594-3.41311 3.44752-3.41311.22051 0 .44378.02112.65793.04138.02304.00218.04597.00435.06878.00649.15725-1.10683.57256-2.13876 1.26949-2.90623.73016-.80404 1.76193-1.30897 3.10143-1.30897 2.4003 0 4.3521 1.9292 4.3521 4.30828 0 .21856.004.35805.0076.4841.0055.19555.0102.35877-.0024.73476.3318.03245.9751.1605 1.5805.50672.7313.41822 1.4158 1.16177 1.4158 2.43286 0 1.3959-1.1444 2.5261-2.5512 2.5261h-1.6509v.8881h1.6509c1.9062 0 3.4518-1.5318 3.4518-3.4142 0-1.70178-1.262-3.11638-2.913-3.37261l-.1432-.02224.0173-.14393c.0245-.20332.0374-.41002.0374-.61945 0-2.86626-2.3524-5.196361-5.2527-5.196361zm-.58683 5.557271 3.77383 3.6085-1.0656 1.01322-1.955-1.86908-.0065 6.88998-1.5124-.0015.00646-6.89308-1.96975 1.87368-1.06252-1.01607zm-3.35678 3.60625.62837.60087 2.26985-2.15912-.00683 7.29342.91239.0009.00684-7.29091 2.25499 2.15581.6303-.59933-3.3397-3.19336z" fill-rule="evenodd"/></g></svg>
                Upload Image
                <input class="hawk__searchInput" type="file" @change="onImageSelect" />
            </label>

            <input type="text" :placeholder="$t(placeholder)" v-model="keyword" @blur="onBlur" />
        </div>

        <div class="hawk__searchFull">
            <span class="hawk__line">
                <input type="text" :placeholder="$t(placeholder)" v-model="keyword" @input="onInput" @keydown="onKeyDown" @blur="onBlur" />
                <svg class="svg-icon" fill="none" height="20" viewBox="0 0 20 20" width="20" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><clipPath id="a"><path d="m0 0h20v20h-20z"/></clipPath><g clip-path="url(#a)"><path clip-rule="evenodd" d="m18.679 16.3218-3.2992-3.2991c.82-1.2659 1.265-2.74 1.265-4.2842 0-2.11084-.8217-4.09667-2.3158-5.58917-1.4933-1.49333-3.4784-2.315834-5.59002-2.315834-2.11166 0-4.09666.822504-5.58916 2.315004-1.49334 1.49333-2.315836 3.47916-2.315836 5.59 0 2.1117.822496 4.0975 2.315836 5.59 1.4925 1.4933 3.47833 2.315 5.58916 2.315 1.54502 0 3.01832-.4433 4.28412-1.2642l3.2992 3.2992c.315.315.7333.4883 1.1783.4883.4451 0 .8634-.1733 1.1784-.4883.315-.3142.4883-.7325.4883-1.1783 0-.4459-.1733-.8642-.4883-1.1784zm-14.35085-3.1733c-1.17833-1.1775-1.8275-2.7433-1.8275-4.41 0-1.66667.64917-3.2325 1.8275-4.41 1.17833-1.17917 2.74417-1.82834 4.41083-1.82834 1.66672 0 3.23252.64917 4.41082 1.82834 1.1783 1.1775 1.8275 2.74333 1.8275 4.41 0 1.6667-.6492 3.2325-1.8275 4.4108-1.1783 1.1792-2.7441 1.8275-4.41082 1.8275-1.66666 0-3.2325-.6483-4.41083-1.8283z" fill="#000" fill-rule="evenodd"/></g></svg>
                <button @click="toggleRequestType">{{ toggleButtonText }}</button>
            </span>
            <button class="image-search-btn" v-if="!imageSearchVisible" @click="toggleImageSearch">
                <svg fill="none" height="20" viewBox="0 0 20 20" width="20" xmlns="http://www.w3.org/2000/svg"><g fill="#000"><path d="m17.2697 20h-14.54291c-.72319 0-1.41676-.2873-1.928131-.7988-.511373-.5115-.798659-1.2052-.798659-1.9285v-14.54543c0-.72331.287286-1.41701.798659-1.928471.511371-.511463 1.204941-.798799 1.928131-.798799h14.54291c.7232 0 1.4168.287336 1.9281.798799.5114.511461.7987 1.205161.7987 1.928471v14.54543c0 .7233-.2873 1.417-.7987 1.9285-.5113.5115-1.2049.7988-1.9281.7988zm-14.54291-18.18182c-.24106 0-.47225.09578-.64271.26627s-.26622.40172-.26622.64282v14.54543c0 .2411.09576.4724.26622.6429.17046.1704.40165.2662.64271.2662h14.54291c.2411 0 .4723-.0958.6427-.2662.1705-.1705.2662-.4018.2662-.6429v-14.54543c0-.2411-.0957-.47233-.2662-.64282-.1704-.17049-.4016-.26627-.6427-.26627z"/><path d="m.909658 15.4547c-.180149.0001-.356278-.0533-.506024-.1534-.149745-.1002-.266353-.2426-.335018-.4092-.06866512-.1666-.0862905-.3498-.0506373-.5264.0356533-.1767.1229763-.3387.2508823-.4656l2.726799-2.7272c.17041-.1691.40077-.2639.64079-.2637.24068.001.47112.0975.6408.2682l2.086 2.0818 5.72175-5.71816c.0844-.08453.1846-.15158.295-.19733.1103-.04575.2286-.0693.348-.0693.1195 0 .2378.02355.3481.0693.1104.04575.2106.1128.295.19733l6.3625 6.36366c.1706.1706.2664.4019.2664.6432 0 .2412-.0958.4726-.2664.6431-.1705.1706-.4018.2665-.643.2665s-.4726-.0959-.6431-.2665l-5.7217-5.72269-5.72175 5.71819c-.16968.1707-.40013.2672-.6408.2682-.11994.0001-.23871-.0236-.34947-.0696s-.21132-.1135-.29587-.1986l-2.08146-2.0818-2.086 2.0863c-.17041.1691-.40077.2639-.640792.2637z"/><path d="m6.36331 8.18177c-.42055-.00033-.82798-.14649-1.15287-.41358s-.54714-.63858-.62889-1.05119c-.08175-.4126-.01793-.84079.18058-1.21161.19851-.37083.51942-.66134.90807-.82205.38865-.1607.82099-.18166 1.22336-.0593.40236.12236.74987.38047.9833.73035.23343.34989.33835.7699.29689 1.18847-.04147.41858-.22676.80983-.5243 1.1071-.34287.33838-.80445.52925-1.28614.53181z"/></g></svg>
            </button>
        </div>

        <search-suggestions :field-focused="fieldFocused" :keyword="keyword"></search-suggestions>
    </div>
</template>

<script>
    import { mapState } from 'vuex'
    import SearchSuggestions from "./SearchSuggestions";
    import CustomResultsLabel from "../results/tools/CustomResultsLabel";
    import { getRecentSearch, setRecentSearch } from '../../CookieHandler';

    export default {
        name: 'search-box',
        props: ['indexName', 'searchPage', 'templateOverride'],
        components: {
            SearchSuggestions,
            CustomResultsLabel
        },
        mounted() {
            this.$root.$on('selectAutocorrectSuggestion', (selectedSuggestion) => {
                this.keyword = selectedSuggestion;
                this.search();
            })
        },
        data() {
            return {
                keyword: null,
                keywordEnter: null,
                placeholder: 'Search with Keywords',
                suggestionDelay: null,
                fieldFocused: false,
                imageSearchVisible: false,
                requestType: 'DefaultSearch',
                toggleButtonText: 'or Concepts'
            }
        },
        methods: {
            search(options = {}) {
                this.cancelSuggestions();

                let searchBoxConfig = this.$root.config.searchBoxConfig;
                let searchPage = this.searchPage || location.pathname;

                this.updateRecentSearch();

                if (searchBoxConfig.redirectToCurrentPage || (this.searchPage && this.searchPage != location.pathname)) {
                    HawksearchVue.redirectSearch(this.keyword, this.$root, searchPage, options.ignoreRedirectRules);
                } else if (this.keyword || searchBoxConfig.reloadOnEmpty) {
                    this.keywordEnter = this.keyword;
                    this.$root.dispatchToStore('fetchResults', {
                        Keyword: this.keyword || "",
                        FacetSelections: {},
                        PageNo: 1,
                        RequestType: this.requestType
                    }).then(() => {
                        HawksearchVue.applyTabSelection(this.$root);
                    });
                }
            },
            updateRecentSearch() {
                setRecentSearch(this.keyword);
                this.$root.$store.commit("updateRecentSearch", getRecentSearch());
            },
            onKeyDown(e) {
                if (e.key === 'Enter') {
                    this.search();
                    e.stopPropagation();
                    e.preventDefault();
                }
            },
            onInput(e) {
                const keyword = e.target.value;

                if (keyword) {
                    this.fieldFocused = true;
                    this.$root.$store.commit('updateLoadingSuggestions', true);

                    clearTimeout(this.suggestionDelay);
                    this.suggestionDelay = setTimeout(() => {
                        this.$root.dispatchToStore('fetchSuggestions', { Keyword: keyword });
                    }, 250);
                } else {
                    this.cancelSuggestions();
                }
            },
            onBlur() {
                setTimeout(() => {
                    if (!this.suggestionClick) {
                        this.fieldFocused = false;
                        this.keyword = this.keywordEnter;
                        this.cancelSuggestions();
                    }
                }, 250);
            },
            onClick(e) {
                e.stopPropagation();
            },
            cancelSuggestions() {
                clearTimeout(this.suggestionDelay);
                HawksearchVue.cancelSuggestionsRequest();
                this.$root.$store.commit('updateLoadingSuggestions', false);
                this.$root.$store.commit('updateSuggestions', null);
            },
            toggleImageSearch() {
                this.imageSearchVisible = true;
                this.requestType = 'ImageSearch';
            },
            closeImageSearch() {
                this.imageSearchVisible = false;
                this.requestType = 'DefaultSearch';
            },
            onImageSelect(event) {
                const file = event.target.files[0];
                if (file) {
                    console.log('Image selected:', file);
                }
            },
            toggleRequestType() {
                if (this.requestType === 'DefaultSearch') {
                    this.requestType = 'ConceptSearch';
                    this.toggleButtonText = 'or Keywords';
                    this.placeholder = 'Search with Concepts';
                } else {
                    this.requestType = 'DefaultSearch';
                    this.toggleButtonText = 'or Concepts';
                    this.placeholder = 'Search with Keywords';
                }
            }
        },
        computed: {
            ...mapState([
                'loadingResults',
                'searchOutput'
            ])
        },
        watch: {
            searchOutput(newValue) {
                if (newValue && newValue.Keyword && newValue.Keyword.length) {
                    this.keyword = newValue.Keyword;
                }
            }
        }
    }
</script>

<style scoped lang="scss">
</style>
