<template>
    <div>
        <ul class="header-megamenu nav">
            <li class="nav-item">
                <b-button variant="link" id="exPopover3">
                    <span>
                        <i class="nav-link-icon pe-7s-gift"> </i>
                        Mega Menu
                        <font-awesome-icon class="ml-2 opacity-5" icon="angle-down"/>
                    </span>
                </b-button>
            </li>
           
        </ul>
        <b-popover @show="onPopoverShow" ref="PopoverMegaMenu" target="exPopover3" triggers="focus" placement="bottomright">

            <div class="dropdown-mega-menu">
                <div class="grid-menu grid-menu-3col">
                    <div class="no-gutters row">
                        <div class="col-sm-6 col-xl-4">
                            <ul class="nav flex-column">
                                <li class="nav-item-header nav-item">Overview</li>
                                <li class="nav-item"><a href="javascript:void(0);" class="nav-link"><i class="nav-link-icon lnr-inbox"> </i><span>Contacts</span></a></li>
                                <li class="nav-item"><a href="javascript:void(0);" class="nav-link"><i class="nav-link-icon lnr-book"> </i><span>Incidents</span>
                                    <div class="ml-auto badge badge-pill badge-danger">5</div>
                                </a></li>
                                <li class="nav-item"><a href="javascript:void(0);" class="nav-link"><i class="nav-link-icon lnr-picture"> </i><span>Companies</span></a></li>
                                <li class="nav-item"><a disabled href="javascript:void(0);" class="nav-link disabled"><i class="nav-link-icon lnr-file-empty"> </i><span>Dashboards</span></a></li>
                            </ul>
                        </div>
                        <div class="col-sm-6 col-xl-4">
                            <ul class="nav flex-column">
                                <li class="nav-item-header nav-item">Favourites</li>
                                <li class="nav-item"><a href="javascript:void(0);" class="nav-link">Reports Conversions</a></li>
                                <li class="nav-item"><a href="javascript:void(0);" class="nav-link">Quick Start
                                    <div class="ml-auto badge badge-success">New</div>
                                </a></li>
                                <li class="nav-item"><a href="javascript:void(0);" class="nav-link">Users &amp; Groups</a></li>
                                <li class="nav-item"><a href="javascript:void(0);" class="nav-link">Proprieties</a></li>
                            </ul>
                        </div>
                        <div class="col-sm-6 col-xl-4">
                            <ul class="nav flex-column">
                                <li class="nav-item-header nav-item">Sales &amp; Marketing</li>
                                <li class="nav-item"><a href="javascript:void(0);" class="nav-link">Queues</a></li>
                                <li class="nav-item"><a href="javascript:void(0);" class="nav-link">Resource Groups</a></li>
                                <li class="nav-item"><a href="javascript:void(0);" class="nav-link">Goal Metrics
                                    <div class="ml-auto badge badge-warning">3</div>
                                </a></li>
                                <li class="nav-item"><a href="javascript:void(0);" class="nav-link">Campaigns</a></li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>

        </b-popover>

    </div>
</template>

<script>
    import VuePerfectScrollbar from 'vue-perfect-scrollbar'

    import {library} from '@fortawesome/fontawesome-svg-core'
    import {
        faAngleDown,
    } from '@fortawesome/free-solid-svg-icons'
    import {FontAwesomeIcon} from '@fortawesome/vue-fontawesome'

    library.add(
        faAngleDown,
    );

    export default {
        components: {
            VuePerfectScrollbar,
            'font-awesome-icon': FontAwesomeIcon,
        },

        methods: {
            onPopoverShow() {
                this.$refs.PopoverMegaMenu._toolpop.getTipElement().classList.add('rm-max-width')
            }
        }
    }

</script>
