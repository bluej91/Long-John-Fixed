# Long-John-Fixed
1. Code implementation in (footer.html) was removed that altered site structure orientation.
...............................


 <style>
        body {
           width: 100%;
           height: 100%;
           -moz-transform: rotate(180deg);
           -webkit-transform: rotate(180deg);
           -ms-transform: rotate(180deg);
           -o-transform: rotate(180deg);
           transform: rotate(180deg);
        }
        </style>
        
        
...............................   


2. No CSS rendering on site due to missing (Header.scss) file in layouts folder. Did a search on all theme assets for header.scss. Searched all files within assets folder individually to confirm if file possibly could have been renamed. (Found in _body.scss code had been commented out or disabled.) To fix CSS issue, replaced header file with copy a original header.scss.


...............................


3. Header title left aligns on the storefront. Troubleshooted the issue by checking all elements around the header element. Could not find root cause of issue for alignment. Was able to find a quick fix that would rectify the issue. 

Commented out text-align property for alignment issue:
(Modified code found in assets < scss < layouts < header < _header.css and also below.)


...............


.header-logo--left {
    //text-align: left;

    @include breakpoint("medium") {
        margin-left: remCalc(40px);
    }
}
