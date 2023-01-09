---
layout: page
title: Papers
subtitle:
---
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/pcooksey/bibtex-js@1.0.0/src/bibtex_js.js"></script>
<bibtex src="\bib\bibi.bib"></bibtex>

<div class="container-fluid">
	<div class="searchbar" >
		<div style="float:left;">
			<button type="button" class="btn btn-default" onclick="reset()">Reset</button>
		</div>
		<div style="float:left;">
			<select id="authorselect" class="btn bibtex_search bibtex_generate_author" style="border: 1px solid lightgrey;" search="author">
			  <option value="">Search Author</option>
			</select>
		</div>
		<div style="float:left;">
			<select id="topicselect" class="btn bibtex_search bibtex_generate_tags" search="tags" bibtex_split_by=", " style="border: 1px solid lightgrey;">
			  <option value="">Search Tags</option>
			</select>
		</div>
		<div style="float:left;">
			<input type="text" class="bibtex_search form-control" id="searchbar" placeholder="Search publications">
			<span class="help-block">Example: journal 2015 (finds the intersection of the two terms)</span>
		</div>
	</div>
</div>

<div class="bibtex_structure">
  <div class="group year" extra="DESC number">
  	  <a href="#top" style="display: inline"><em>(Top of the page)</em></a>
  	  <div style="padding-bottom:10px;"></div>
  	  <div class="sort journal" extra="DESC string">
      	<div class="templates"></div>
      </div>
  </div>
</div>

<div id="bibtex_display">
    <div class="bibtex_template"> <!--callback="cullabstract(bibtexentry)">-->
        <table>
            <tr>
                <td width="250" height="100" style="text-align:center">
                    <div class="if img">
                        <img class="bibtexVar" src="\img\papers\+img+" img width="250" extra="img" />
                    </div>
                </td>
                <td>
                    <!-- TITLE -->
                    <div>
                        <span class="if projecturl">
                            <a class="bibtexVar"  href="+PROJECTURL+" extra="projecturl">
                                <span style="text-decoration: underline;" class="title"></span>,
                            </a>
                        </span>
                        <span class="if !projecturl">
                            <span class="if paperurl">
                                <a class="bibtexVar"  href="+PAPERURL+" extra="paperurl">
                                    <span style="text-decoration: underline;" class="title"></span>,
                                </a>
                            </span>
                            <span class="if !paperurl">
                                <span style="text-decoration: underline;" class="title"></span>
                            </span>
                        </span>
                    </div>
    
                    <!-- AUTHORS -->
                    <span class="author"></span>
    
                    <!-- DETAILS -->
                    <div>
                        <span class="if journal"><em><span class="journal"></span></em>,</span>
                        <span class="if publisher"><em><span class="publisher"></span></em>,</span>
                        <span class="if booktitle">In <em><span class="booktitle"></span></em>,</span>
                        <span class="if address"><span class="address"></span>,</span>
                        <span class="if month"><span class="month"></span>,</span>
                        <span class="if year"><span class="year"></span>.</span>
                        <span class="if note"><span class="note"></span></span>
                        <span class="if award"><span style="color:red" class="award"></span></span>
                    </div>
                    <span hidden class="tags"></span>
    
                    <!-- COLLAPSABLES -->
                    <div>
                        <!-- project page link -->
                        <span class="if projecturl">
                            <a class="bibtexVar"  href="+PROJECTURL+" extra="projecturl">
                                [Project Page]
                            </a>
                        </span>
                        
                        <!-- expand raw bibtex -->
                        <a class="bibtexVar" role="button" data-toggle="collapse" href="#bib+BIBTEXKEY+" aria-expanded="false" aria-controls="bib+BIBTEXKEY+" extra="BIBTEXKEY" bibtexjs-css-escape>
                            [Bibtex]
                        </a>
    
                        <!-- expand abstract -->
                        <span class="if abstract">
                            <a class="bibtexVar" role="button" data-toggle="collapse" href="#abstract+BIBTEXKEY+" aria-expanded="false" aria-controls="abstract+BIBTEXKEY+" extra="BIBTEXKEY" bibtexjs-css-escape>
                                [Abstract]
                            </a>
                        </span>
                        
                        <!-- paper link -->
                        <span class="if paperurl">
                            <a class="bibtexVar"  href="+PAPERURL+" extra="paperurl">
                                [PDF]
                            </a>
                        </span>
                    </div>
                </td>
            </tr>
        </table>
        <div class="bibtexVar collapse" id="bib+BIBTEXKEY+" extra="BIBTEXKEY">
            <div class="well" style="word-wrap: normal;">
            <pre><span class="bibtexraw noread" id="citation"></span></pre>
            </div>
        </div>
        <div class="bibtexVar collapse" id="abstract+BIBTEXKEY+" extra="BIBTEXKEY">
            <div class="well">
            <span  style="word-wrap: normal;" class="abstract"></span>
            </div>
        </div>
    </div>
</div>


<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
<!--<script>
    function cullabstract(bibtexentry) {
        var bibtexentry = bibtexentry[0];
        var span = bibtexentry.getElementById("citation");
        var text = span.textcontent;
        text = text.slice(0,text.indexOf("cutafter="));
        span.textcontent = text;
    }         
</script>-->

